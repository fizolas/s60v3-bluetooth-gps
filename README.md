Sharing GPS of s60v3 phone with computer running Debian 11 (Bullseye) through Bluetooth

Put s60v3-bluetooth-gps script in ~/bin or some other directory in the path, and make it executable (chmod +x s60v3-bluetooth-gps)

Put yourself in the sudoers group: e.g. for user john: "usermod -aG sudo john" (for this to be effective you need to log out and log in again)

Pair your phone with your computer; set the computer as "authorised" in the bluetooth menu of the phone

Run "s60v3-bluetooth-gps phone_name" to tether the phone with bluetooth name "phone_name"

Start GPS sharing in your phone, if you have not done so already (e.g. Symartic ExtGPS, which is a j2me app), remember to switch on Bluetooth on the phone

You can now use Linux/Debina applications which recognise gpsd, such as cgps or foxtrotgps (both signs in Symartic ExtGPS will be green when there is a GPS lock and bluetooth connection)

Ctrl-C stops the tethering session leaving the system consistent

Tethering works well with two different phones I've tried (E52, E72)

Note: for the Evolution email client to work during tethering, set "Method to detect online state" to "base" in "Settings>Network Preferences"
