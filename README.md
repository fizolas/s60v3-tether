# s60v3-tether
Bluetooth tethering of s60v3 phones in Debian 11 (Bullseye)

Put wvdial.conf in /etc, write IP of your internet provider (and username and paswword if needed)

Put s60v3-tether script in ~/bin, and make it executable (chmod +x)

Pair your phone(s) with your computer; give access permission to the computer from the phone(s) in the bluetooth menu

List your phone(s) in the "case" region in the script s60v3-tether: in the example given, phone_name has bluetooth address ff:ff:ff:ff:ff:ff and dial-up is on channel 1

(in order to find the bluetooth address you can use "hcitool scan"; then use "sdptool browse bluetooth_address" to find dial-up channel)

Finally run "s60v3-tether phone_name" to tether the phone through bluetooth

Ctrl-C stops the session and restores network manager

I have three phones in my case list (two of them s60v3 FP2 and one s60v3 FP1), and thethering works well with them all, although the connection sometimes drop with the FP1

Note: for evolution to work during tethering, in Settings>Network Preferences set "Method to detect online state" to "base"
