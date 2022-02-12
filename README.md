# s60v3-tether
Bluetooth tethering of s60v3 phones in Debian 11 (Bullseye)

Put wvdial.conf in /etc
Put s60v3-tether script in ~/bin, and make it executable (chmod +x)
Pair your phone(s) with your computer; give access permission to the computer from the phone(s) in the bluetooth menu
List your phone(s) in the "case" region in the script: in the example, phone_name has bluetooth address ff:ff:ff:ff:ff:ff and dial-up is in channel 1
(in order to find bluetooth address use hci tool scan, then use sdptool browse bluetooth_addresss to find dial-up channel)
Finally run s60v3-tether phone_name to tether the phone through bluetooth
Ctrl-C stops the session and restores network manager

I have three phones in the case list (two s60v3 FP2 and one s60v3 FP1), and thethering works with them all
