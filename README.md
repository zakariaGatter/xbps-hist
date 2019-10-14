# Xbps-hist

## Table of Contents

- [About](#about)
- [Quick Start](#quick-start)
- [Using Xbps-hist](#using-zshing)
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
	* __Socklog-void__ : Void Linux socklog configuration

2. Set up [Xbps-hist]:

	``` bash
	git clone https://gitlab.com/zakariaGatter/xbps-hist.git ~/brash
	mkdir -p ~/.local/bin
	cp ~/xbps-hist/bin/xbps-hist ~/.local/bin
	chmod +x ~/.local/bin/xbps-hist
	```

## Using Xbps-hist

```
XBPS-HIST
Write by Zakaria Gatter (zakaria.gatter@gmail.com)

Command Line Xbps Log Viewer

xbps-hist [OPTS]

OPTS :
    -a|--action : What [ACTIONS] you looking for
    -d|--date   : Set date and time to search
    -l|--list   : List all packages
    -s|--search : Search for speacial Package
    -f|--full   : Show full View
    -h|--help   : Show this help dialog

ACTIONS :
    install : any use of xbps-install
    remove  : any use of xbps-remove
    update  : any use of xbps-install -Su

NOTE :
    - the search start from the day you install socklog-void and enable (socklog-unix nanoklogd) add gatter to socklog GROUND
    - Valide date and time : YYYY-MM-DD HH:MM:SS
```

## TODO
[Xbps-hist] is a work in progress, so any ideas and patches are appreciated.

[Xbps-hist]:http://gitlab.com/zakariagatter/xbps-hist
