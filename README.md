# s60v3-tether
Bluetooth tethering of s60v3 phones in Debian 11 (Bullseye)

Put wvdial.conf in /etc and replace "data.provider.com" with the IP of your own internet provider (complete Username and Paswword, if needed)

Put s60v3-tether script in ~/bin or some other directory in the path, and make it executable (chmod +x s60v3-tether)

Put yourself in the sudoers group: e.g. for user john: "usermod -aG sudo john" (for this to be effective you need to log out and log in again)

Pair your phone with your computer; set the computer as "authorised" in the bluetooth menu of the phone

Run "s60v3-tether phone_name" in a terminal to tether the phone with bluetooth name "phone_name"

Ctrl-C stops the tethering session leaving the system consistent (both during dial-up channel search or during wvdial)

Tethering works well with three different phones I've tried (E63, E52, E72), although the connection sometimes drops with the E63 (s60v3 FP1)

Note: for the Evolution email client to work during tethering, set "Method to detect online state" to "base" in "Settings>Network Preferences" 
