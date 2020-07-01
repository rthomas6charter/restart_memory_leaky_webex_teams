# Instructions
* Copy the plist file to /System/Library/LaunchDaemons
  * This will probably require admin/sudo/superuser access
* Copy the workflow directory (automator script bundle) to /user/bin
* If the automator script bundle directory is located somewhere other than /usr/bin/restart_memory_leaky_webex_teams.workflow, edit the copy of the plist file accordingly.
* Load the launch daemon
  * **sudo launchctl load -w /System/Library/LaunchDaemons/com.example.restart-memory-leaky-webex-teams.plist**

# Test
* (After copying the automator script bundle directory into /usr/bin/, from a terminal window execute command:
  * **automator /usr/bin/restart_memory_leaky_webex_teams.workflow**

# References
* http://www.robzand.com/blog/use-automator-on-mac-to-restart-applications
* https://stackoverflow.com/questions/132955/how-do-i-set-a-task-to-run-every-so-often
* https://superuser.com/questions/373813/how-do-i-run-an-automator-action-shell-script-or-applescript-on-startup-in-os-x
* https://superuser.com/questions/126907/how-can-i-get-a-script-to-run-every-day-on-mac-os-x
