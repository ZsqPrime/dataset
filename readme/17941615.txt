# transmission-remote-dotnet
Automatically exported from code.google.com/p/transmission-remote-dotnet

## About
transmission-remote-dotnet is a Windows remote client to the RPC interface of transmission-daemon, which is part of the Transmission BitTorrent client. The application is quite like µTorrent in appearance and currently supports almost all the RPC specification.

## transmission-remote-dotnet 3.24.3 (12/11/11)
Fixed tracker filter issue
Updated geoip database
## transmission-remote-dotnet 3.24.2 (19/10/11)
Fixed two issue at new Transmission
## transmission-remote-dotnet 3.24.1 (17/10/11)
Add support to new Transmission (>2.40)
## transmission-remote-dotnet 3.24 (13/12/10)
New release with following features:

* issue 71 	Enhancement idea: RSS
* issue 219 	Support Other SSH Clients (cygwin)
* issue 221 	No "Default" server means confusing to add server details. Server settings greyed out. Need "Add Server" button
* issue 223 	Enhancement: selecting destination folder when using Add torrent from URL
* issue 225 	Enhancement idea: selected items summary in bottom bar
* issue 226 	UI Fixes: ETA sorting and Date formats (Lowest Priority)
* issue 231 	Ratio reported incorrectly
* issue 232 	Open folder menu item
* issue 233 	Tray icon showing status
* issue 235 	Info about remote server's transmission version(s)
* issue 240 	Plink should use -l -t options
* issue 246 	Move data on completion
* issue 249 	Different refresh rate when docked/minimized
* issue 250 	Show progress bar in Done column
* issue 254 	Transmission ID
* issue 262 	Statistics
* issue 268 	Filter
* issue 274 	Memorise left panel size (+minor translation improvements)
* issue 277  Colorize the Ratio-Display
* issue 285  Default settings\permanent amount of peers per torrent
* issue 299  Double-Click to Launch/Preview
* issue 322  More than 5 entry stored in directory download drop-down list

## Features
* French, German, Danish, Hungarian, Chinese, Polish, Turkish, Russian, Korean, Spanish, Czech, Dutch, Brazilian. translations.
* Supports all or almost all the remote functionality of Transmission.
* Adding torrents by handling .torrent files, drag-n-drop, and browsing.
* Optional add .torrent prompt to choose wanted files and priorities, set destination directory and peer limit.
* Start, stop, remove, delete, recheck, move torrents.
* Authentication support.
* Limiting upload/download/peer/ratio limits globally or for specific torrents. Set alternate global limits for certain times.
* Prioritisation of files and torrents.
* Remotely update the blocklist and test the incoming BitTorrent port.
* Filter by tracker or state.
* Proxy support.
* Minimise/close to tray option, torrent complete/started popup.
* Country of peers displayed by text and flag using GeoIP.
* SSL support.
* Multiple settings profiles.
* More!
