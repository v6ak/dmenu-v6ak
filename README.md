dmenu-v6ak
==========

My script to run dmenu. Features:
* simple history support (Recent commands are preffered. You can reorder the recent command manually via file.)
* custom blacklist (you can exclude commands you don't use)
* cached menu
* items listen in lines
* colors close to Ubuntu's Ambiance theme

Requirements:
* bash etc. :)
* dmenu
* zenity
* libnotify-bin

Notes on caching:
* Unless you are on a Debian-based distro, you should change `PACKAGE_LOG` variable.
* Cache is rebuilt in foreground or in background, depending on cache invalidation trigger.
	* When a package log (i.e. `/var/log/dpkg.log`) is modified, is may mean a new app is added. However, it often means an update. So, the cache is updated in background.
	* When an important file (e.g. config or the script itself) is changed, it is considered to be an important change and cache is updated in foreground, which may delay the startup time.

History:
The history file is intentionally made to be compatible with gRun. If you want to change order of items or remove an item, just edit `~/.config/dmenu_v6ak/history`. The most important items are on the bottom of this file.

