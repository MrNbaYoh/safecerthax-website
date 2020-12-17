---
layout: single
title: "User Guide"
permalink: /user-guide/
toc: true
author_profile: true
---

**Warning:** safecerthax is an exploit for **O3DS/2DS only**, it does **not** work on N3DS & N2DS. For more information, please check out the [FAQ](/faq/).
{: .notice--warning}

This guide provides instructions on how to use safecerthax to install [boot9strap](https://github.com/SciresM/boot9strap) through the [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller).

## Section I: Getting started

1. Download the latest [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases) archive.
2. Extract its content and copy the `SafeB9SInstaller.bin` file to the root of your 3DS SD card.

From there, there are two different ways of using safecerthax:
- You can [use the public safecerthax DNS & NUS servers](#section-ii-using-the-public-dns--nus-servers).
- You can [setup your own safecerthax-proxy server](#section-iii-setting-up-your-own-safecerthax-proxy) (more technical).

## Section II: Using the public DNS & NUS servers

**WARNING:** safecerthax uses an exploit in the 3DS SSL system module to bypass SSL/TLS certificate verifications. It means that you're **not safe** when using custom DNS or proxy servers. Thus, I highly recommend not using any proxy or DNS server other than the ones provided here. Moreover, you should stop using the safecerthax servers once you have finished using the exploit. I am not responsible for any issue caused by the use of potential untrusted third-party servers.
{: .notice--danger}

1. Power on your 3DS and launch the System Settings application.
2. Navigate to `Internet Settings` -> `Connection Settings`.
3. Tap on your network connection slot and navigate to `Edit` -> `DNS` -> `Advanced Settings`.
4. Tap on `Yes` and edit both fields as follows:
  - `Primary DNS`: `54.38.133.70`
  - `Secondary DNS`: `54.38.133.70`
5. Save your changes and run the connection test.
6. If the test succeeded, you may now shutdown your device and go to [Section IV](#section-iv-running-the-exploit).

## Section III: Setting up your own safecerthax-proxy
*TODO*


## Section IV: Running the exploit

The exploit does not have a 100% success rate. It might freeze or get stuck on a black screen. If this occurs, just retry from step 1 of Section IV. However, if your problem persists, please check out the [Troubleshooting section of the FAQ](/faq/#troubleshooting).
{: .notice--info}

1. Power on your device in Recovery Mode by pressing `L+R+Up+A` on startup.
2. Tap on `OK` and `I Aggree` when it asks you to connect to the Internet to update your device.
3. Tap on `OK` to begin the fake update.
4. The update should fail and an error message should pop up.
5. Close the error message.
6. The exploit should run and launch SafeB9SInstaller.
