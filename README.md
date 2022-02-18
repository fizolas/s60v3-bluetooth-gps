Sharing of GPS receiver from s60v3 phone with computer running Debian 11 (Bullseye) through Bluetooth

Put s60v3-bluetooth-gps script in ~/bin or some other directory in the path, and make it executable (chmod +x s60v3-bluetooth-gps)

Put yourself in the sudoers group: e.g. for user john: "usermod -aG sudo john" (for this to be effective you need to log out and log in again)

Pair your phone with your computer; set the computer as "authorised" in the bluetooth menu of the phone

Run "s60v3-bluetooth-gps phone_name" to share the GPS receiver of the phone with bluetooth name "phone_name"

Start sharing the GPS receiver in your phone, if you have not done so already: you can do it by running Symarctic ExtGPS, a J2ME app (do not forget to switch on Bluetooth on the phone)

You can now use any Linux/Debian applications that recognises gpsd, such as foxtrotgps (maps, tracks), navit (car navigation) or cgps (GPS data).

The two circles in Symarctic ExtGPS will turn from red to green when there is both a GPS fix and an active bluetooth connection (note: even if the phone is connected to the computer, the bluetooth circle only turns green when you are running a gpsd application)

Ctrl-C stops the session, leaving the system consistent

GPS sharing works well with two different phones I've tried (E52, E72)

You can simultaneously have a tethered internet connection (using the s60v3-tether script in a separate terminal) and GPS from the same phone through bluetooth in your computer, as different rfcomm devices are used in the s60v3-tether and s60v3-bluetooth-gps scripts
