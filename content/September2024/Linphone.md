+++
title = 'How To set Up Linphone with SIP Credentials Using TLS'
date = 2024-09-12T23:30:13-04:00
draft = true
+++

So I decided to get a VOIP or Voice Over IP phone number for several reasons.  I don't have any illusions about actually remaining anonymous on the internet or anywhere else.  Gradually, I hope to expand my skillset, however, so that maybe every little thing I do is not tracked. If you find this interesting then check out Rob Braxman at [BraxMe](https://brax.me/).

After you have acquired a VOIP number and SIP credentials, you will need a way to use them.  A softphone, like [Linphone](https://linphone.org), which is open source under the GNUv3 licence, is perfect.  You do not actually need a physical phone for your number.  You can use your PC or chromebook even.  [Linphone](https://linphone.org) is available for Linux, Windows, MacOS, iOS and Android.  I use my VOIP number as my main number now.

Firstly, [download Linphone](https://new.linphone.org/technical-corner/linphone?qt-technical_corner=2#qt-technical_corner) to your device or install it from, for example Ubuntu repository like so...

sudo apt update
sudo apt install linphone

Then search for linphone using whatever desktop manager you have installed.  Once this is accomplished and you have the app open, tap on the menu icon (the 4 parallel horizontal bars) at the top left.

Next choose ASSISTANT. On the ASSISTANT screen, tap USE SIP ACCOUNT and click I UNDERSTAND in response to the displayed message.  Here is where we enter our SIP credentials.   

Under USERNAME enter the username given by your SIP provider.  Next enter the password.  Now enter your DOMAIN or REALM.  This will look something like

sip.example.com

If you are going to stay with UDP which is more forgiving and ever so slightly faster then this is the end of the line.  You can now make calls, text and even video call with your [Linphone](https://linphone.org) app.  

That is cool if you ask me!

However, let's be a little paranoid because this is the internet in 2024.  We will go ahead and set up TLS with TCP.

Go back to the main menu and select SETTINGS from the menu icon.  Now select CALL.  We will now set MEDIA ENCRYPTION to SRTP and turn on MEDIA ENCRYPTION MANDATORY.  Lastly, click on the CONNECTED next to the green circle.  On the resultant screen,  change the TRANSPORT OPTION to TLS.

And that's it!  Hope this helps!
