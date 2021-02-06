## MyDwm

dwm is an extremely fast, small, and dynamic window manager for X.

## Requirements

In order to build dwm you need the Xlib header files.

- compiz
## Installation

Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install

## Patches applied
- [x] 添加透明度 [dwm-alpha-20201019-61bb8b2.diff.diff](https://dwm.suckless.org/patches/alpha/)
- [x] 自启动 [dwm-autostart-20161205-bb3bd6f.diff](https://dwm.suckless.org/patches/autostart/)
- [x] 在状态栏显示所有的窗口名称 [dwm-awesomebar-20191003-80e2a76.diff](https://dwm.suckless.org/patches/awesomebar/)
- [x] 全屏某个窗口 [dwm-fullscreen-6.2.diff](https://dwm.suckless.org/patches/fullscreen/)
- [ ] 只显示有窗口的标签 [dwm-hide_vacant_tags-6.2.diff](https://dwm.suckless.org/patches/hide_vacant_tags/)
- [x] 当只有一个窗口可见时，删除边框 [dwm-noborder-6.2.diff](https://dwm.suckless.org/patches/noborder/)
- [x] 不同的标签拥有不同的窗口管理方式 [dwm-pertag-20200914-61bb8b2.diff](https://dwm.suckless.org/patches/pertag/)
- [ ] 移动窗口到其他标签之后,标签跟着一起移动到制定位置 [dwm-r1522-viewontag.diff](https://dwm.suckless.org/patches/viewontag/)
- [x] 循环调整窗口到栈顶[dwm-rotatestack-20161021-ab9571b.diff](https://dwm.suckless.org/patches/rotatestack/)
- [dwm-scratchpad-6.2.diff](https://dwm.suckless.org/patches/scratchpad/)
- [dwm-vanitygaps-20200610-f09418b.diff ](https://dwm.suckless.org/patches/vanitygaps/)


## Running dwm

Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

```bash
DISPLAY=foo.bar:1 exec dwm
```

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

```bash
while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
do
    sleep 1
done &
exec dwm
```

## Configuration

The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
