# AutoCAD plugin developer test assignment

Please create an AutoCAD plugin in C#, using AutoCAD dependencies from NuGet, you could target AutoCAD 2025 or 2026.
The plugin must add a new button into the main Ribbon (you can add an image to it, but it doesn't really matter).
Pressing this button shall trigger a command written in C#, which does the following:

* Gets user's current IPv4 address (e.g. from https://ipv4.icanhazip.com)
* Creates an MTEXT entity and changes its value to IP address retrieved in the previous point
* Then MTEXT element must be rotated by 90.5 degrees clockwise or anti-clockwise
* Load DWG file, it could be locally stored, it must be a heavy one, e.g. https://www.cadforum.cz/catalog_en/block.asp?blk=25475
* Show a WPF progress bar while loading the file, hide it when the loading process has finished
* (Optional) Write a log message "Plugin execution finished!" into a log file, you have to get an instance of the logger via dependency injection
