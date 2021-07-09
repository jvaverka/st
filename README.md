# st - simple terminal

st is a simple terminal emulator for X which sucks less.

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit `config.mk` to match your local setup (st is installed into
the `/usr/local` namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

```shell
make clean install
```

## Settings

Can be done through `Xresources` -
see [Xdefaults](https://github.com/LukeSmithxyz/st/blob/master/Xdefaults)
for example.

## Patches

Patches applied in order:

| patch | file |
--- | ---
| xresource | st-xresources-20200604-9ba7ecf.diff |
| alpha | st-alpha-0.8.2.diff |
| anysize | st-anysize-0.8.4.diff |
| desktopentry | st-desktopentry-0.8.4.diff |
| boxdraw | st-boxdraw_v2-0.8.3.diff |
| ligatures | st-ligatures-boxdraw-20200430-0.8.3.diff |
| appsync | st-appsync-20200618-b27a383.diff |
| font2 | st-font2-20190416-ba72400.diff |
| clipboard | st-clipboard-0.8.3.diff |
| scrollback | st-scrollback-0.8.4.diff |
| scrollback-mouse | st-scrollback-mouse-20191024-a2c479c.diff |
| scrollback-mouse-altscreen | st-scrollback-mouse-altscreen-20200416-5703aa0.diff |
| bold is not bright | st-bold-is-not-bright-20190127-3be4cf1.diff |
| externalpipe | st-externalpipe-0.8.4.diff |
| externalpipe* | st-externalpipe-eternal-0.8.3.diff |

*Using [st-handler](https://github.com/LukeSmithxyz/st/blob/master/st-urlhandler)

***all patches in `patches` directory***

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

```shell
tic -sx st.info
```

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

Heavily inspired by these two configs

- https://github.com/ChristianChiarulli/st
- https://github.com/LukeSmithxyz/st
