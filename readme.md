# About
Certain versions of Cisco Webex Teams for Mac just eat up more and more memory while they're running,
until they're restarted.  If Teams is allowed to run long enough, OSX will finally pop up an alert
that system memory is all used up.  This is a simple Mac automator script and launcher (.plist) to
automatically restart Webex Teams every day.

* Note: This could be adapted to restart just about anything on just about any schedule.

# Instructions
* Copy the com.example.restart-memory-leaky-webex-teams.plist file to /System/Library/LaunchDaemons
  * This will probably require admin/sudo/superuser access
* Copy the workflow directory (automator script bundle) to /user/bin
* Load the launch daemon
  * **sudo launchctl load -w /System/Library/LaunchDaemons/com.example.restart-memory-leaky-webex-teams.plist**

* Note: If the automator script bundle directory is located somewhere other than /usr/bin/restart_memory_leaky_webex_teams.workflow, edit the copy of the plist file accordingly.
* Note: If you'd like the restart to happen some other time of day, edit the args in the "StartCalendarInterval" section of the plist file.

# Test
* (After copying the automator script bundle directory into /usr/bin/, from a terminal window execute command:
  * **automator /usr/bin/restart_memory_leaky_webex_teams.workflow**

# References
* http://www.robzand.com/blog/use-automator-on-mac-to-restart-applications
* https://stackoverflow.com/questions/132955/how-do-i-set-a-task-to-run-every-so-often
* https://superuser.com/questions/373813/how-do-i-run-an-automator-action-shell-script-or-applescript-on-startup-in-os-x
* https://superuser.com/questions/126907/how-can-i-get-a-script-to-run-every-day-on-mac-os-x

# Updates
* 2021/1/22 - Changed the start path to match the install location of the current version of Webex + Webex Teams
  * Cisco has apparently consolidated some of the processes that run on a Mac.
  * Also no longer sure if the memory issues persist.  This automator script may not be necessary now.
