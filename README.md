whatsapp-blue
=============

This project it's in its early development stage. Come back later! :squirrel:

New here? Take a moment to read this

## Protocol
The WhatsApp protocol is sadly not officially documented. 

The protocol is based on the XML-based XMPP protocol, a heavily documented
internet messaging protocol. To reduce the XML overhead, the XML structure and a
lot of common keywords are converted into bytes. See docs/funxmpp.txt for a
more detailed explanation. Sadly, the XMPP standard is not followed exactly
everywhere.

* Protocol wrapper: FunXMPP (see Wiki)
* Main protocol: XMPP (http://xmpp.org/rfcs/rfc6120.html)
* Authentification: SASL, digest auth (http://tools.ietf.org/html/rfc2831)
* Blocking: XMPP privacy lists? (http://xmpp.org/extensions/xep-0016.html)
* Ping (http://xmpp.org/extensions/xep-0199.html)

### Encryption

Following the news that WhatsApp messages were sent in plaintext (and thus
readable for everyone when on a WiFi hotspot), encryption was added. At least
the Android client uses this encryption, which seems to be TLS as specified by
the XMPP RFC. However, I did not really look into this. Also, the mapping of
keywords to bytes seems to have also changed in the latest version of the
Android app.


FAQ
---

### How do I get my user name and password?

Your user name is your phone number (including the country code but without any
additional leading zeros, e.g. `4917012345678`), as for the password there are
many ways to get it. You can either sniff it or just ask for a new one. Check
these links here:

* https://github.com/venomous0x/WhatsAPI#faq
* https://github.com/shirioko/MissVenom
* http://blog.philippheckel.com/2013/07/05/how-to-sniff-the-whatsapp-password-from-your-android-phone-or-iphone/

If you want to register a new WhatsApp account, you can use tools like yowsup
or WART:

* https://github.com/tgalal/yowsup
* https://github.com/shirioko/WART

Please, do not contact me by email for this kind of issues, I won't answer your
questions. For developing matters you can open an issue, create a pull request
or (in case you think it's necessary) email me.


Disclaimer
-----------

WhatsApp is a registered trademark of WhatsApp Inc registered in the U.S. and
other countries. This project is an independent work and has not been authorized,
sponsored, or otherwise approved by Whatsapp Inc. 
