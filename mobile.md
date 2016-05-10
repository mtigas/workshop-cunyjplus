# Mobile tools

## Signal

**Signal**, by [Open Whisper Systems](https://whispersystems.org/).
  * Download: [iPhone](https://itunes.apple.com/us/app/signal-private-messenger/id874139669), [Android](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms&referrer=utm_source%3DOWS%26utm_medium%3DWeb%26utm_campaign%3DMessaging)
  * End-to-end encryption for voice calls and messages inside the app.
  * Accounts: Uses phone numbers to register and as a way for you to find your contacts. (Doesn't send your contacts list to their servers, at least.)
  * Metadata: You trust Open Whisper Systems with message metadata.
  * Trustable: open-source, audited, experts like it, backed by well-regarded staff and developer community


## Other apps

**iMessage**
  * Has [good end-to-end encryption](https://www.apple.com/business/docs/iOS_Security_Guide.pdf) but only works with Mac/iOS.
  * Accounts: AppleID needs an email address and/or phone number.
  * Metadata: You trust Apple with message metadata.
    * And if you back up your phone to iCloud, your message history is stored in the cloud -- maybe defeating your end-to-end encryption.
  * Trustable: design is documented (but not open-source), audited, backed by the most valuable company in the world

**WhatsApp**
  * Good end-to-end encryption: Open Whisper Systems (creators of Signal) helped up the security of WhatsApp as of this year.
    * The tech behind Signal and WhatsApp is so good that Brazil jailed a Facebook VP for a day, because Facebook didn't have any way to decode messages that the government wanted -- they could only get the metadata.
  * Accounts: Phone number.
  * Metadata: You trust Apple with the metadata.
    * And if you back up your phone to iCloud, your message history is stored in the cloud -- maybe defeating your end-to-end encryption.
  * Trustable: design is documented (but not open-source), audited, backed by a very large company

**Threema**
  * End-to-end encryption.
  * Accounts: You use a randomly-generated ID (and QR code) instead of a username or your e-mail address or phone number.
    * (You can add your e-mail address or phone number so others can find you, or keep the random ID to keep yourself somewhat anonymous.)
  * Metadata: You trust Threema with metadata.
    * The pseudonymous ID helps... a little bit.
  * Trustable: Design is documented (not open-source), audited.

**Snapchat**
  * Only encrypted between you and Snapchat. The company can see everything.
  * Their [privacy policy](https://www.snapchat.com/privacy) says they delete content when it expires, but they can't promise it's totally inaccessible:

    > It’s also possible, as with any digital information, that someone might be able to access messages forensically or find them in a device’s temporary storage. Keep in mind that, while our systems are designed to carry out our deletion practices automatically, we cannot promise that deletion will occur within a specific timeframe. And we may also retain certain information in backup for a limited period of time or as required by law.

**Facebook Messenger**
  * Only encrypted between you and Facebook. The company can see everything.
