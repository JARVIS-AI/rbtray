# RBTray

RBTray is a small Windows program that runs in the background and allows almost any window to be minimized to the system
tray by:

- Right-Clicking its minimize button
- Shift-Right-Clicking on its title bar
- Using the Windows-Alt-Down hotkey

Note that not all of these methods will work for every window, so please use whichever one works for your needs.

RBTray is free, open source, and is distributed under the terms of the
[GNU General Public Licence](http://www.gnu.org/copyleft/gpl.html).

## Download

The latest binaries can be downloaded by going to the
[build actions page](https://github.com/benbuck/rbtray/actions?query=workflow%3ABuild) and clicking on te top item in
the list. You should see an "artifact" link that will download a zip file that contains both Debug and Release builds of
RBTray.

![Build](https://github.com/benbuck/rbtray/workflows/Build/badge.svg)

Not that RBTray previously had separate 32 and 64 bit binary builds, but now only has 64 bit. If you really need the 32
bit version, please let me know.

These are the binaries for the [original RBTray](http://sourceforge.net/projects/rbtray/files/).

## Installing

- Download the binaries.
- Unzip the download.
- Open either the Debug or Release (preferred) folder.
- Double click RBTray.exe to start it.

If you want it to automatically start after you reboot:

- Create a location where RBTray should be permanently located (e.g. `C:\Program Files\RBTray`).
- Copy RBTray.exe and RBHook.dll to that location.
- Open the Start menu's Startup group, located at `"%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup"`, which can
also be by pressing "`WIN` + `R`" then typing `shell:Startup`.
- Create a shortcut to RBTray.exe in the Startup folder.

## Using

To minimize a program to the system tray, you can use any of these methods:

- Right-click with the mouse on the program's minimize button.
- Hold the Shift key while Right-clicking on the program's title bar.
- Pressing Windows-Alt-Down on the keyboard (all at the same time).

This should create an icon for the window in the system tray. To restore the program's window, single-click the
program's icon in the tray. Alternatively, you can Right-click on the tray icon which should bring up a popup menu, then
select Restore Window.

In some cases the first two methods cause problems with other software because of they way they integrate into Windows
using a hook to intercept mouse events. In this case, you can use the `--no-hook` option, which means that only the last
method of using a hotkey will work. Also the RBHook.dll isn't needed since it only exists to support the mouse event
hook.

## Exiting

Right click on any tray icon created by RBTray and click Exit RBTray in the popup menu, or run RBTray.exe with the
`--exit` parameter.

## Authors

Nikolay Redko: http://rbtray.sourceforge.net/, https://github.com/nredko

J.D. Purcell: http://www.moitah.net/, https://github.com/jdpurcell

Benbuck Nason: https://github.com/benbuck

## Other

For original forum, bug tracker, etc. see [RBTray SourceForge project page](http://sourceforge.net/projects/rbtray/).

Copyright &copy; 1998-2011 Nikolay Redko, J.D. Purcell

Copyright &copy; 2015 Benbuck Nason
