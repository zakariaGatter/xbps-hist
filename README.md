# Xbps-hist

## Table of Contents

- [About](#about)
- [Quick Start](#quick-start)
- [Using Xbps-hist](#using-zshing)
- [Examples](#examples)
- [TODO](#todo)

## About


[Xbps-hist] xbps Log Viewer

[Xbps-hist] allows you to...

* List all Actions in log file
* List by Action
* List by Date
* Search for a Package
* Search for a Package in a Date
* Search for a Package with a Action

[Xbps-hist] automatically...

* check for correct Date or Action

[Xbps-hist] is undergoing an interface change, please stay up to date to get latest changes.

## Quick Start

1. Introduction:

   Installation requires :
	* [Socklog-void](https://github.com/voidlinux/socklog-void) : Void Linux socklog configuration
    * [Coreutils](https://www.gnu.org/software/coreutils) for Everything else

2. Set up [Xbps-hist]:

	``` bash
	git clone https://gitlab.com/zakariaGatter/xbps-hist.git ~/brash
	mkdir -p ~/.local/bin
	cp ~/xbps-hist/bin/xbps-hist ~/.local/bin
	chmod +x ~/.local/bin/xbps-hist
	```

## Using Xbps-hist

```
Usage: xbps-hist [OPTIONS] [PKGNAME...]

OPTIONS                                                                                                                                    -
 -a --action <act>  What [ACTIONS] you looking for
 -d --date <date>   Set date and time to search
 -l --list          List all packages
 -s --search <pkg>  Search for speacial Package
 -f --full          Show full View
 -h --help          Show this help dialog

ACTIONS
 install         any use of xbps-install                                                                                                   -
 remove          any use of xbps-remove
 update          any use of xbps-install -Su

NOTE
 the search start from the day you install socklog-void and enable (socklog-unix nanoklogd) add $USER to socklog GROUND
 Valide date and time : YYYY-MM-DD HH:MM:SS
```

## Examples

* Show everything in the log
    `xbps-hist -l`

* Show everything with a action
    `xbps-hist -a install -l`

* Show eberything with a action and a date
    `xbps-hist -a install -d "2019-10-21 13:38:00" -l`

* Search for package
    `xbps-hist -s socklog-void`

* Search for package with action
    `xbps-hist -a install -s socklog-void`

* Search for package with action and date
    `xbps-hist -a install -d "2019-10-21 13:38:00" -s socklog-void`

## TODO
[Xbps-hist] is a work in progress, so any ideas and patches are appreciated.

[Xbps-hist]:http://gitlab.com/zakariagatter/xbps-hist
