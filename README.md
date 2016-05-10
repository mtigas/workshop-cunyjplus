# CUNY J+ Online Security Workshop

You can find this file -- containing all the links -- at https://github.com/mtigas/workshop-cunyjplus


# Current Events & Background

* Reporters working on national security, document leaks, government affairs
  * [Panama Papers](https://panamapapers.icij.org/), Snowden, etc.
  * [Apple vs FBI](http://www.nytimes.com/2016/02/18/technology/explaining-apples-fight-with-the-fbi.html)
* Cell phone subpoenas
  * [2013 DoJ gets phone records of AP reporters](http://www.theguardian.com/world/2013/may/13/america-government-associated-press-phone-records)
* Libel suits opening up e-mail & chat records
  * Newsroom chat logs opened up in [Hulk Hogan v Gawker](http://nymag.com/selectall/2016/03/what-hulk-hogan-taught-me-about-slack.html)
  * An Android developer made a joke in an e-mail years ago and [it appeared in court yesterday](https://twitter.com/xor/status/730062894147117056) as evidence.

The internet isn't magic. Security isn’t magic.

In the real world, things move from point A to point B all the time. You don't expect a piece of mail to magically appear at your friend's house once you drop it into a mailbox. Just like the postal service, there's a whole system built to relay what you do on the internet.

Postcards are a simple type of message, but they let anybody (your mail carrier and anyone snooping on your mailbox) read the entire message.

You use envelopes or boxes to hide everything except the metadata:
Return address, destination, size/weight, when you sent it.

What if, instead of an envelope that your recipient opens, you had an envelope that got opened at the post office (so your mail carrier can't read your message)? That's sort of how e-mail works right now.

Most encryption tools try to be like that envelope that works all the way from your end to your friend's end. The tools protect what they can, but you'll need to have some metadata for things to get moved around properly.

Traditionally, phone calls worked like postcards, too. (And right now, they still sort of work like the envelope that gets opened at the post office. There's no guarantee at all that a phone call is secure the rest of the way.)

Enough metaphors. What's metadata look like?

* The outside of envelopes.
* Call logs.
* Billing records.
* Browser history.
* Access logs on websites.

You can tell a lot from metadata alone, but revealing metadata is often a lot better than revealing everything you're doing.

# Tool recommendations

We're here to install software, aren't we?

Note: for all of the communication tools, the person you’re contacting will also need to have the tool installed. (Otherwise, how would they decode your secure message?)

Open-source vs closed.
What providers to trust.

## Mobile Tools

**Signal**, by [Open Whisper Systems](https://whispersystems.org/).
  * Download: [iPhone](https://itunes.apple.com/us/app/signal-private-messenger/id874139669), [Android](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms&referrer=utm_source%3DOWS%26utm_medium%3DWeb%26utm_campaign%3DMessaging)
    * https://whispersystems.org/
  * End-to-end encryption for voice calls and messages inside the app.
  * Accounts: Uses phone numbers to register and as a way for you to find your contacts. (Doesn't send your contacts list to their servers, at least.)
  * Metadata: You trust Open Whisper Systems with message metadata.
  * Trustable: open-source, audited, experts like it, backed by well-regarded staff and developer community

---

*[More notes here](mobile.md) other mobile apps (like iMessage, Facebook Messenger, WhatsApp, Snapchat, etc.)*

**Other mobile advice**

* Please use a passcode. Don't use anything shorter than 6 digits.
  * On iOS, enabling a passcode encrypts the phone. If you make too many wrong guesses, the phone gets wiped.
  * On Android, depending on your phone, there are a few extra steps to encrypt your phone.
  * If your phone isn't encrypted, be wary of having your phone stolen and be wary of what you plug your phone into.
* Metadata: Apple and Google know you downloaded the apps
* You're still using a handheld computer.

## Laptop Tools

### Web Browsing: Plugins

**HTTPS Everywhere**
  * [Download for Chrome & Firefox](https://www.eff.org/https-everywhere)
    * https://www.eff.org/https-everywhere
  * If a website has an optional encrypted version ("HTTPS"), this will make your browser use that whenever possible.

**uBlock Origin**, by "gorhill"
  * Download: [Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm), [Firefox](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)
  * Block malware on websites, and maybe make your web browsing faster.
    * If you have moral reservations about blocking advertising, you can choose to only block malware: Click uBlock icon, click "gear" for settings, "3rd-party filters" tab, and then un-check everything the first "uBlock filters" box and everything under "Ads" and "Privacy". (Leave the "Auto update" and "Parse and enforce" boxes at the top checked.) [See here](images/ublock-only-malware.png).

### Web Browsing: Anonymity

**Tor Browser Bundle**
  * [Download](https://www.torproject.org/download/download-easy.html.en)

Tor hides your IP address from the website you're visiting.

It also has built-in encryption that can help you get around censorship, whether you're in a foreign country, or if you're at an office that blocks certain websites.

Tor Browser Bundle has HTTPS Everywhere and an ad-blocker built-in.

### Messaging

**Ricochet**: Encrypted chat
  * [Download](https://ricochet.im/)
  * Uses Tor under the hood.
  * End-to-end encryption.
  * No Accounts: No account registration. Randomly-generated user IDs.
  * Metadata: No central servers. Your computer makes an encrypted connection directly to your friend's computer. (Your ISP will know that you're using Tor.)

**Tor Messenger**: Encrypted chat
  * [Download](https://trac.torproject.org/projects/tor/wiki/doc/TorMessenger)
  * Relies on an existing chat network. You can use independent chat servers or Google Chat.
  * End-to-end encryption.
  * Accounts: Still relies on existing accounts at a chat server.
  * Metadata: The chat service still sees all metadata.

**Jitsi**: Encrypted video calls
  * A competitor to Google Hangouts, Skype, GoToMeeting, etc.
  * Like the Hangouts site, there's no download. [Just use the website](https://meet.jit.si/).
    * https://meet.jit.si/
  * End-to-end encryption.
  * No accounts: You get a link for your video call that you share with your friends. It lasts until you're done.
  * Metadata: The service still knows the metadata.

**Google Chat**, **Google Hangouts**, **Skype**, **Slack**, **Facebook Messenger**, etc.
  * Only encrypted between you and the organization. The company running the service can see your messages, access your calls, and see all metadata.

### Email & files

**PGP**
  * What Edward Snowden used to reach out to Laura Poitras and Glenn Greenwald.
    * [There’s even a Windows tutorial that he anonymously sent to Greenwald](https://vimeo.com/56881481)
  * What a lot of technologists and activists have been using since the 90's. (It's only improved _a little bit_ since the 90's.)
  
**GPG** (**GnuPG**) is one version of PGP. The names are exchangable.

A few ways to set it up:

**Thunderbird** & **Enigmail**
  * Download Thunderbird
    * https://www.mozilla.org/thunderbird/
  * Download Enigmail
    * https://enigmail.net/
  * When you're done setting up Thunderbird, open up the Addons menu ([see here](images/thunderbird-addons.png)), click the "gear" icon and choose "Install Add-on from file..." ([see here](images/thunderbird-addons2.png)).

**Windows Outlook** & **GPG4Win**
* Download GPG4Win
  * https://www.gpg4win.org/
* Tutorial: https://www.youtube.com/watch?v=Y2U5RzWLEHI (2:30 - 13:40)

**Mac Mail app** & **GPGTools**
* Download GPGTools
  * https://gpgtools.org/
* Guide: https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-mail

**Mailvelope** in your web browser
* Download for Chrome or Firefox
  * https://www.mailvelope.com/
* Tutorial: https://www.youtube.com/watch?v=xKDk3l6nRc4 (1:15 - 11:03)


# Further Reading

New tools come out all the time and often make claims about security. The EFF created a scorecard with ProPublica that has some good criteria you should consider:

* https://www.eff.org/secure-messaging-scorecard

Other helpful guides to installing security software or thinking about a threat model:

* https://pressfreedomfoundation.org/encryption-works
* https://source.opennews.org/en-US/learning/security-journalists-part-one-basics/
