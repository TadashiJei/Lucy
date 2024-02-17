<h1 align="center">🔒 Lucy 🔒</h1>
<p align="center">This Bash script installs and runs the Lucy tool, a wireless security auditing tool used to perform attacks such as WPA/WPA2 cracking and MITM attacks.</p>

[![LOGO](https://img.shields.io/github/issues/0n1cOn3/termux-wifi?style=plastic)]() [![LOGO](https://img.shields.io/github/issues-pr/0n1cOn3/termux-wifi?style=plastic)]() [![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)

___📋 Requirements :___

- A device running Termux (latest Lucy Release only supports ARM64 (64bit)
- Internet connection

## 💻 Usage

Clone this repository or download and extract the script file
Open the terminal and navigate to the script directory.
```
git clone https://github.com/TadashiJei/Lucy.git
```
Run the script with the following command:

    ./lucy_installer.sh

The script will install all necessary dependencies, download and install the Fluxion tool, and start the Fluxion tool. (Ubuntu chroot)

## :book: How it works
* Scan for a target wireless network.
* Launch the `Handshake Snooper` attack.
* Capture a handshake (necessary for password verification).
* Launch `Captive Portal` attack.
* Spawns a rogue (fake) AP, imitating the original access point.
* Spawns a DNS server, redirecting all requests to the attacker's host running the captive portal.
* Spawns a web server, serving the captive portal which prompts users for their WPA/WPA2 key.
* Spawns a jammer, deauthenticating all clients from original AP and luring them to the rogue AP.
* All authentication attempts at the captive portal are checked against the handshake file captured earlier.
* The attack will automatically terminate once a correct key has been submitted.
* The key will be logged and clients will be allowed to reconnect to the target access point.

## 👥 Credits

- Original script by Tadashi_Jei
- Maintained by Lucyfer

## ⚠️ Disclaimer

This script is intended for educational purposes only. 
The use of this script for attacking targets without prior mutual consent is illegal. 
It is the end user's responsibility to obey all applicable local, state, and federal laws. The authors of this script assume no liability and are not responsible for any misuse or damage caused by this script.
