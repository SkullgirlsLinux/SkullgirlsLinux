# Skullgirls
Below are a list of useful FAQ:


Why does my Controller not show up?

We are only supporting controllers which will work in Steam Big Picture mode if your controller is not configured to work with Steam Big Picture it will not show up.

1. Click the controller icon at the top right of Steam to enter Big Picture mode.
2. Click the cog next to the clock to open up the “Settings” menu.
3. Once in the Settings menu click “Controller“ and “Edit Controller” to map your controller to an XInput style layout.
4. Once you have added and saved your controller you should now be able to use it in Skullgirls.

If you have any issues with controller setup please check out the Steam Big Picture group here:
http://steamcommunity.com/groups/BigPicture

If you wish to check what controller config Steam is sending to the game we have included the launch option “-copymappings” which will dump the string to the clipboard when you launch Skullgirls. If your custom Steam Big Picture controller mapping is not there then either you have not set it up correctly or there is an issue with Steam sending the mapping to the game, please report the issue at the BigPicture group.


Where should I report bugs?

You may report bugs and issue to our github issues tracker at https://github.com/SkullgirlsLinux/Skullgirls
Please only report bugs that you are able to replicate (occur more than once).


What should I do if the game crashes?

Crash dumps for Linux can be found in /tmp/dumps/ please send these to us and we will take a look. 
If the game freezes and becomes unresponsive DO NOT force quit as it will not create a dump! 
You will need to attach gdb to the process and send us the backtrace.

Find out the process id (PID) either by looking in your System Monitor or via the “ps” command.
Once you know the SkullGirls process id you may start gdb using the following commands:

You will either need sudo or su access or the ability to ptrace applications.
Try one the following commands:
sudo gdb -p PID
su -c "gdb -p PID" 

Then send us the output from:
thread apply all bt

