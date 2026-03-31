Github ngvincent Oppo Kernel Source
=========================================

This repository contains the kernel source code for Oppo Find 5 (x909), with changes added.

Official source code: https://github.com/oppo-source/Find5-Kernel-Source

How to build from this repository
-----------------------------------

If you wish to build the kernel on your local machine, check the pages below for a tutorial

https://git.ngvincent.com/projects/oppo-x909-cm10/wiki/Build-kernel (always the most-updated version

http://forum.xda-developers.com/showthread.php?t=2192805 (clone of the page above, not updated as frequently)

XDA: http://forum.xda-developers.com/forumdisplay.php?f=2155


How my branches are structured
<pre>
----- master ( forked and commits updated from official oppo source)
        | 
      make-fixes (include any config fixes needed to compile without problems from master. no code changes here)
        | --------
                | stable branch (contains code changes deemed stable)
                ----------| experimental branches (experimental changes for testing)
</pre>