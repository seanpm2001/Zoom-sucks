# Zoom Sucks

* Zoom abuses the installer flow on MacOS to bypass permissions dialogs ([source](https://twitter.com/c1truz_/status/1244737672930824193))
* Zoom sends identifying device info to Facebook, even when users don't have a Facebook account ([source](https://www.vice.com/en_us/article/k7e599/zoom-ios-app-sends-data-to-facebook-even-if-you-dont-have-a-facebook-account)) ([fixed](https://www.vice.com/en_us/article/z3b745/zoom-removes-code-that-sends-data-to-facebook))
* A bug in Zoom sent identifying information (including email addresses and profile pictures) of thousands of users to strangers ([source](https://www.vice.com/en_us/article/k7e95m/zoom-leaking-email-addresses-photos))
* Zoom claims that meetings are end-to-end encrypted in their white paper and marketing materials, but meetings are only encrypted in transit, and are available in plaintext to Zoom servers and employees. ([source](https://theintercept.com/2020/03/31/zoom-meeting-encryption/))
* `zoomAutenticationTool` can be used to escalate privileges of arbitrary scripts/programs ([source](https://twitter.com/DanAmodio/status/1245032929635586053))
* Another method of privilege escalation involving the `AuthorizationExecuteWithPrivileges` API during the installation process ([source](https://9to5mac.com/2020/04/01/new-zoom-bugs-takeover-macs-cam-mic-root/))
* Zoom browser extension grants unnecessary access to full browser history ([source](https://gist.github.com/lrvick/c56957437dd1b7d11eb22bee0c6b2792#browser-plugin))
* Zoom browser extension has unrestricted TCP access on 0.0.0.0 ([source](https://gist.github.com/lrvick/c56957437dd1b7d11eb22bee0c6b2792#browser-plugin))
* Zoom MacOS client runs an insecure local web server to bypass standard app URI flows. This web server can be abused to initiate video/audio recording without the user's consent ([source](https://www.macrumors.com/2019/07/09/zoom-videoconferencing-app-vulnerability/))
* Zoom Windows client can be used to send SMB network share credentials to an attacker ([source](https://arstechnica.com/information-technology/2020/04/unpatched-zoom-bug-lets-attackers-steal-windows-credentials-with-no-warning/))
* Zoom MacOS client specifically disables library validation, allowing attacker libraries to be loaded into its address space ([source](https://9to5mac.com/2020/04/01/new-zoom-bugs-takeover-macs-cam-mic-root/))
* Zoom lies about using AES-256 encryption. In fact, Zoom uses AES-128 (which is less secure) in ECB mode (which is *dangerously* insecure) ([source](https://citizenlab.ca/2020/04/move-fast-roll-your-own-crypto-a-quick-look-at-the-confidentiality-of-zoom-meetings/))
* A bug in Zoom routed calls from North America and Europe through Chinese datacenters, against Zoom's promise that meetings are only routed through the jurisdictions of the meeting's participants ([source](https://techcrunch.com/2020/04/03/zoom-calls-routed-china/))
* Facebook sign-in can be added to any account without email confirmation, allowing complete control over the account to an attacker ([source](https://medium.com/@s3c/how-i-hacked-worldwide-zoom-users-eafdff94077d)) (fixed)

## Zoom Devices

Zoom devices include smart TVs, tablets, and smart cameras. Most of these devices include cameras and microphones and are typically installed within line of sight and earshot of sensitive conversations.

* Zoom devices (such as smart cameras and tablets) downloaded unsigned firmware updates over HTTP, leaving them vulnerable to man in the middle attacks (fixed)
* Zoom devices run Linux 2.6.2, with 600+ reported vulnerabilities as of March 2020
* Zoom device bootloader is unlocked, allowing root shell access during boot
* Root password is set to default

[Source](https://gist.github.com/lrvick/c56957437dd1b7d11eb22bee0c6b2792#evaluation)
