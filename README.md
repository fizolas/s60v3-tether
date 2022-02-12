# s60v3-tether
Bluetooth tethering of s60v3 phones in Debian 11 (Bullseye)

Put wvdial.conf in /etc, replace "data.provider.com" with the IP of your own internet provider (complete Username and Paswword if needed)

Put s60v3-tether script in ~/bin or some other directory in the path, and make it executable (chmod +x)

Put yourself in the sudoers group: e.g. for user john: "usermod -aG sudo john" (for this to be effective you need to log out and log in again)

Pair your phone(s) with your computer; give access permission to the computer from the phone(s) in the bluetooth menu

List your phone(s) in the "case" region in the s60v3-tether script (three examples are given in the script): you need to provide in each case a name, the bluetooth address, and the dial-up channel

In order to find the bluetooth address of the phone you can use "hcitool scan, then use "sdptool search --bdaddr bluetooth_address DUN" to find the corresponding dial-up channel.

Finally run "s60v3-tether phone_name" to tether the phone listed as "phone_name"

Ctrl-C stops the tethering session and restores network manager

I have three phones in my case list (two of them s60v3 FP2 and one s60v3 FP1), and thethering works well with them all, although the connection sometimes drops with the FP1 phone

Note: for evolution to work during tethering, in Settings>Network Preferences set "Method to detect online state" to "base"

Note: if things fail, check the dial-up channel, sometimes it changes "magically"...
