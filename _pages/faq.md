---
layout: single
title: "FAQ"
permalink: /faq/
toc: true
---

# General Q&A

#### How does safecerthax work?

safecerthax uses [SSLoth](https://github.com/MrNbaYoh/3ds-ssloth) to bypass SSL/TLS certificate verifications and spoof 3DS system update servers (NUS). The safecerthax DNS redirects requests to a custom fake NUS server. The custom NUS server triggers a fake system update that exploits an old vulnerability in the O3DS & 2DS recovery mode firmware (SAFE_FIRM).

For more information, please check out the [safecerthax repository](https://github.com/MrNbaYoh/safecerthax) and the [write-up](/write-up/).

#### Is it safe to use safecerthax?
Yes it is, at least as safe as any other full chain exploit.

Though, considering [SSLoth](https://github.com/MrNbaYoh/3ds-ssloth) is a thing, you should avoid using custom DNS and proxy servers. safecerthax servers are safe, but on this point, you have no choice but to trust me.

#### What is SSLoth exactly?
For more information on SSLoth, please visit the [SSLoth repository]((https://github.com/MrNbaYoh/3ds-ssloth).

#### Will safecerthax ever work on N3DS & N2DS?
Unfortunately, it won't ever work on N3DS & N2DS devices. safecerthax uses some very old vulnerabilities that firmware version 5.0.0 fixed on NATIVE_FIRM (the regular firmware). The O3DS/2DS recovery mode firmware (SAFE_FIRM) is based on a very old firmware revision that is still vulnerable to those flaws. The N3DS/N2DS SAFE_FIRM is much more recent and based on firmware version 8.0.0 that is not vulnerable.

#### Can I setup my own safecerthax proxy/server?
Yes you can, both the [safecerthax-proxy](https://github.com/MrNbaYoh/safecerthax-proxy) and [safecerthax-server](https://github.com/MrNbaYoh/safecerthax-server) are open source and available on GitHub.
For complete instructions on how to setup a local safecerthax proxy, please check out the [User Guide](/user-guide/).

#### My shoulder button is broken, am I screwed?
Yes you are. Booting into safe mode requires holding `L+R+Up+A` at startup. If you cannot get it to work, you should probably try another exploit such as seedminer.

# Troubleshooting

If you encounter an issue that is not listed here, or if your problem persists, please create a detailed issue ticket in the [safecerthax GitHub repository](https://github.com/MrNbaYoh/safecerthax/issues) (device model, region, firmware version etc.). You can also hit me up on [Twitter](https://twitter.com/MrNbaYoh) or seek for help on the [Nintendo Homebrew discord server](https://discord.gg/C29hYvh).
{: .notice--info}

#### After configuring the safecerthax DNS in my network settings, the connection test fails...
First, you should check that you have entered the right IP address. If there is no mistake, the DNS server might be down, just wait and try again later.

#### When running the exploit, an error message pops up, but after closing it, the device shuts down...
First, check that you have correctly configured the DNS. If there is no mistake, either the DNS or the custom NUS server might be down, just wait and try again later.

#### When running the exploit, it gets stuck or freezes...
The exploit does not have a 100% success rate, try again, it should work eventually.

#### When running the exploit, a crash occurs...
Try again. If the problem persists, please create a detailed issue ticket in the [safecerthax GitHub repository](https://github.com/MrNbaYoh/safecerthax/issues).
