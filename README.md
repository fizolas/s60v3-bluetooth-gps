Sharing of GPS receiver from s60v3 phone with computer running Debian 11 (Bullseye) through Bluetooth

Put s60v3-bluetooth-gps script in ~/bin or some other directory in the path, and make it executable (chmod +x s60v3-bluetooth-gps)

Put yourself in the sudoers group: e.g. for user john: "usermod -aG sudo john" (for this to be effective you need to log out and log in again)

Pair your phone with your computer; set the computer as "authorised" in the bluetooth menu of the phone

Run "s60v3-bluetooth-gps phone_name" to tether the phone with bluetooth name "phone_name"

Start sharing your GPS in your phone, if you have not done so already. You can do it by starting Symarctic ExtGPS, a J2ME app. Do not forget to switch on Bluetooth on the phone.

You can now use any Linux/Debian applications that recognise gpsd, such as cgps or foxtrotgps.

The two circles in Symarctic ExtGPS will turn from red to green when there is both a GPS lock and an active bluetooth connection. Even if the phone is connected through bluetooth, the bluetooth circle only turns green when you are using cgps or foxtrogps

Ctrl-C stops the session, leaving the system consistent

GPS sharing works well with two different phones I've tried (E52, E72)
