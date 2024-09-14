+++
title = 'How To set Up Linphone with SIP Credentials Using TLS'
date = 2024-09-12T23:30:13-04:00
draft = false
+++

So I decided to get a VOIP or Voice Over IP phone number for several reasons.  I don't have any illusions about actually remaining anonymous on the internet or anywhere else.  Gradually, I hope to expand my skillset, however, so that maybe every little thing I do is not tracked. If you find this interesting then check out Rob Braxman at [BraxMe](https://brax.me/).

After you have acquired a VOIP number and SIP credentials, you will need a way to use them.  A softphone, like [Linphone](https://linphone.org), which is open source under the GNUv3 licence, is perfect.  You do not actually need a physical phone for your number.  You can use your PC or chromebook even.  [Linphone](https://linphone.org) is available for Linux, Windows, MacOS, iOS and Android.  I use my VOIP number as my main number now.

Firstly, [download Linphone](https://new.linphone.org/technical-corner/linphone?qt-technical_corner=2#qt-technical_corner) to your device or install it from, for example, Ubuntu repository like so...

sudo apt update

sudo apt install linphone

Then search for linphone using whatever desktop manager you have installed.  Once this is accomplished and you have the app open, tap on the menu icon (the 4 parallel horizontal bars) at the top left.

{{< figure src="/images/linphone/Screenshot_20240913-132320.png" width="250" >}}
{{< figure src="/images/linphone/Screenshot_20240913-220316.png" width="250" >}}

Next choose ASSISTANT. On the ASSISTANT screen, tap USE SIP ACCOUNT.

{{< figure src="/images/linphone/Screenshot_20240913-132335.png" width="250" >}}

Click I UNDERSTAND in response to the displayed message.  {{< figure src="/images/linphone/Screenshot_20240913-132350.png" width="250" >}}   Here is where we enter our SIP credentials.

{{< figure src="/images/linphone/Screenshot_20240913-132406.png" width="250" >}}

Under USERNAME enter the username given by your SIP provider.  Next enter the password.  Now enter your DOMAIN or REALM.  This will look something like

sip.example.com

Your SIP provider probably has a slightly different address for you based on whether you are using UDP or TLS so enter the right one!  If you are going to stay with UDP which is more forgiving and ever so slightly faster then this is the end of the line.  You can now make calls, text and even video call with your [Linphone](https://linphone.org) app.  

That is cool if you ask me!

However, let's be a little paranoid because this is the internet in 2024.  We will go ahead and set up TLS with TCP because security!

Go back to the main menu and select SETTINGS from the menu icon.

{{< figure src="/images/linphone/Screenshot_20240913-132424.png" width="250" >}}

 Now select CALL.

 {{< figure src="/images/linphone/Screenshot_20240913-132440.png" width="250" >}}

 We will now set MEDIA ENCRYPTION to SRTP and turn on MEDIA ENCRYPTION MANDATORY.  

 {{< figure src="/images/linphone/Screenshot_20240913-132440.png" width="250" >}}

 Lastly, click on the CONNECTED next to the green circle.  On the resultant screen,  change the TRANSPORT OPTION to TLS.

 {{< figure src="/images/linphone/Screenshot_20240913-220408.png" width="250" >}}

And that's it!  Hope this helps!
