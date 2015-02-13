# motionscripts

Motion <http://www.lavrsen.dk/foswiki/bin/view/Motion/WebHome> is a very useful software motion detection that I have been running for the past year or so on old PCs and even on a Raspberry Pi.

Detecting motion is an essential component of a security system, but I also needed real-time notification and immediate backup.  There were a couple of scripts around, none of which fulfilled my requirements, so I wrote these two and they have been working pretty well since last Summer.

Features:
  * Immediate notification by email or SMS (optional) with attached picture
    enables nearly real-time assessment of the situation and immediate reaction
  * Immediate offsite backup of the captured images with rsync/ssh
    prevents destruction of the captured evidence even if the camera is
    damaged / stolen during the break in

Hardware Requirements and Considerations:
  * Any modern x86 computer, or a Raspberry Pi.  Might work on other platforms
  * Any compatible USB camera (more restrictive for Raspberry Pi)
  * Recommended: UPS backup

Software Requirements:
  * Tested on Debian and Ubuntu, likely to work on most Linux/Unix system
  * Motion
  * Python (tested with 2.7.6) and dependencies
  * rsync
  * SSH

Service Requirements:
  * Internet connection with decent upload capacity
  * A hosted server.  Any hosted Linux/BSD with SSH/rsync/SMTP and a web server will do.  I have tried backing up to Dropbox but the latency was unpleasant
  * Optional: a Twilio account

These scripts have been helpful to me, I hope they are to you too!

Yuv