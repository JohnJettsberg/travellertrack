# Traveller Ship Tracker

A shared tracker for ships, finances, crew and businesses in a **Mongoose Traveller
2nd Edition** campaign. One person (the host) runs the server; everyone else opens
the website and logs in.

> Not a virtual tabletop. It tracks ships as living assets: stats, upgrades,
> mortgage and maintenance, crew, cargo and trade.

## For players

Open the website, then enter the **Server URL** your host gives you and log in
with the account your host created for you (or Google sign-in if they enabled it):

**https://johnjettsberg.github.io/travellertrack/**

## For hosts: download Traveller Host

Traveller Host is a desktop app that runs the server and manages accounts, data,
backups and port forwarding. Get the newest version from the
**[latest release](https://github.com/JohnJettsberg/travellertrack/releases/latest)**
and pick the file for your system:

| System | Recommended | Alternative |
|--------|-------------|-------------|
| Windows | [Installer (.exe)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.0/Traveller-Host-0.2.0-win-x64.exe) | [Portable (.zip)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.0/Traveller-Host-0.2.0-win-x64.zip) |
| macOS (Apple Silicon) | [Disk image (.dmg)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.0/Traveller-Host-0.2.0-mac-arm64.dmg) | [Zip](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.0/Traveller-Host-0.2.0-mac-arm64.zip) |
| Linux (x64) | [AppImage](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.0/Traveller-Host-0.2.0-linux-x86_64.AppImage) | [Archive (.tar.gz)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.0/Traveller-Host-0.2.0-linux-x64.tar.gz) |

These links are for version 0.2.0. Newer versions are always on the
**[latest release page](https://github.com/JohnJettsberg/travellertrack/releases/latest)**.

The apps are not code-signed, so your system will warn you the first time:

- **Windows:** SmartScreen → **More info** → **Run anyway**.
- **macOS:** right-click the app → **Open**. If it says the app is "damaged", run
  `xattr -cr "/Applications/Traveller Host.app"` in Terminal.
- **Linux:** make the AppImage executable (`chmod +x`) and run it. Recent
  Ubuntu/Debian may need `sudo apt install libfuse2`.

### Getting started as a host

1. Open Traveller Host and click **Start server**.
2. Open **Accounts** and create your admin account, then accounts for your players.
3. **Same home network:** players use `http://YOUR-LAN-IP:8787`. The app shows the address.
4. **Friends elsewhere:** open **Port Forwarding** and click **Enable port forwarding**,
   or use a free HTTPS tunnel such as Cloudflare Tunnel. Port forwarding is plain
   HTTP, so only share the address with people you trust.
5. Keep the app open while your group plays. Use **Back up database** regularly.

An HTTPS website (like the one above) cannot talk to a plain HTTP server on the
internet, so friends outside your network need the HTTPS tunnel. On your own
computer or your home network, the tracker page served by the app itself works
without one.

## Data and legal

Your data stays on the host's computer. Bundled game data comes from openly
licensed sources (the Traveller SRD / OGL and community open data). This is an
unofficial fan project. Traveller is a trademark of its owners and this project
is not affiliated with Mongoose Publishing.
