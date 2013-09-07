watchme
=======
Window usage data collector and analyzer script for MS Windows.

Written by Jonathan Foote (jmfoote@andrew.cmu.edu)


Description
===========
watchme.py is a Python script that polls to collect information about the active window in your window manager. It only works on Windows. The script can be controlled  via a the task icon it adds the system tray after it is launched. In addition to tracking window information, it also includes some basic data analysis capabilities.


WARNING!
========
This script will collect data about what you do on your system and store it in plaintext to your local filesystem. USE THIS SCRIPT AT YOUR OWN RISK -- there is no warranty, and I take NO responsibility for what you do with it, or anything that happens to you as a result of using it.


Usage
=====
Run watchme.py via python from the commandline:

  python watchme.py

Or, to "install" it, create a batch script to run it with pythonw and add a shortcut to the batch script to your Startup folder.

  pythonw watchme.py


Dependencies
============
Requires pywin32: http://sourceforge.net/projects/pywin32/
  
Background
==========

This is a toy application that I developed as a result of thinking about how cognitive load is affected by task switching and decrease in productivity (and increase in defect rate) that results from working in certain environments. Ostensibly this script could be extended to work on Linux, OSX (and all of the other platforms that modern devs use) so that information could be aggregated across systems and give you an accurate picture of what you are working on. These were my thoughts before I found out that "time cockpit" existed (I haven't tried it, but it looks cool, and this is more or less what it is trying to accomplish). Anyway, feel free to hack this up, as I may not go anywhere with it myself :) This script is very simple, but if you have any questions or comments feel free to drop me a line at jmfoote@andrew.cmu.edu.


TODOs
=====

[x] Daemonize & survive Windows sleeping (works with python.exe, but not pythonw.exe)
[x] Add idle time logging
[x] Gather licenses for included open source code
[x] Add license to text to readme and warn about privacy implications
[ ] Add install/egg
[ ] Beef up readme to include example and internals info
[x] Make icon
[ ] Publish to github
[ ] Add support for exe name processing to analyzer
[ ] Add support for idle_time/window_time processing to analyzer
[ ] Add additional analysis: histrograms, search by exe name, etc.
[ ] Implement lock/some sort of singleton to prevent running proc twice
[ ] Add ML :)
[ ] Add support for aggregating data across machines (for VM use)
[ ] Add support for other desktop managers
[ ] Become a rich philanthropist, etc.

Licenses
========

See LICENSE.txt for details on the licenses of this project and included open source code