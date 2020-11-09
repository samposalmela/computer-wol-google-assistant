# <img src="https://raw.githack.com/FortAwesome/Font-Awesome/master/svgs/solid/desktop.svg" card_color="#D80DE5" width="50" height="50" style="vertical-align:bottom"/>Turning computer on with Google Assistant

I made this referring to [TopHATTwaffle's Youtube video](https://www.youtube.com/watch?v=iD6lCh7Uhq8).

What you need:
- Google Assistant
- [IFTTT](https://ifttt.com/)
- [Pushbullet](https://play.google.com/store/apps/details?id=com.pushbullet.android&hl=fi&gl=US)
- [Automagic](https://play.google.com/store/apps/details?id=ch.gridvision.ppam.androidautomagicworkarounds&hl=fi)

## 1. Configure your computer to wake up with LAN

Go to Settings > Network & Internet > Change adapter options > Ethernet > Properties > Congigure > Power Management

Choose
- Allow this device to wake the computer
- Only allow a magic packet to wake the computer

(NOTE: If you don't see the Power Management option go to Advanced > Wake on magic packet and choose value as Enabled. You may also have to Enable Wake on LAN from BIOS. For this refer to your Motherboard BIOS manual.)

## 2. Make IFTTT applet

Sign in or make an account for IFTTT. 

Go to Create and then choose "If This add"

Search for "Google Assistant" and choose that.

Choose "Say as simple phrase" and then fill in the needed blanks to your preference.

After that choose "Then That add".

Search for "Pushbullet" and choose that. 

Choose "Push a note" and fill in the blanks.

(NOTE: Make sure the message is filled with something that is not used by another pushbullet used by you.)

Then choose "Create action" and click "Finish"

## 3. Configure Automagic

Press the "+" to create a new flow.

Click the empty box and press the menu button and then press the "New..." button in the bottom left corner.

Choose "Plugin Event".

Choose Plugin as "Received a Push"

Enter what you put as a message to IFTTT for Pushbullet as containing text. 

Then press "Save".

Then drag the "+" next to your created Plugin Event to add an action. Choose "Action". After that choose "New..." and choose "Send Wake on LAN Packet".

Press the three dots (...) located on the left of "MAC address" and enter your IP address.

(NOTE: If you don't know your IP address, press WINKEY + R > Type "cmd" > press ENTER > Type "ipconfig" > press ENTER > IPv4 Address)

Then Automagic should automatically fill in your MAC address.

(NOTE: If it does not autofill, press WINKEY + R > Type "cmd" > press ENTER > Type "ipconfig /all" > press ENTER > Physical address, and enter it manually to Automagic.)

Then fill in the IP/Port where the start is your IPv4 address and the last three digits after the last dot are replaced by 255.

Then press "Save".

Then enable the flow by pressing the switch in the top right corner. 
