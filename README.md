# Traveller Ship Tracker

A shared tracker for ships, finances, crew and businesses in a **Mongoose Traveller
2nd Edition** campaign. One person (the host) runs the server; everyone else uses
the website or the separate Traveller Tracker player app.

> Not a virtual tabletop. It tracks ships as living assets: stats, upgrades,
> mortgage and maintenance, crew, cargo and trade.

## For players

Open the website, enter the **Server URL** your host gives you (usually an
`https://` link) and sign in with the account your host created for you, or with
Google sign-in if your host enabled it:

**https://johnjettsberg.github.io/travellertrack/**

### Standalone Traveller Tracker app

Desktop releases built with the player-app update also include **Traveller
Tracker**, separate from **Traveller Host**. Check the
[latest release assets](https://github.com/JohnJettsberg/travellertrack/releases/latest)
for files starting with `Traveller-Tracker-` (older releases contain Host only):

| System | Installer / application | Archives |
|--------|-------------------------|----------|
| Windows (x64) | `.exe` installer | Portable `.zip` |
| macOS (Apple Silicon) | `.dmg` | `.zip` |
| Linux (x64) | `.AppImage` | `.tar.gz` and `.zip` |

Tracker includes the built website and star-map snapshot; it does **not** load
the GitHub website or run a game server. Enter the Host's Server URL and sign in.
Accounts, shared worlds and game data still need a running Host. It accepts
HTTP LAN/port-forwarded addresses as well as HTTPS, without disabling browser
security. HTTP is unencrypted: prefer HTTPS for internet access.

Google opens in your system browser (Google does not support embedded-browser
OAuth), then returns the result automatically to the initiating app. Keep the
app open and allow the browser's localhost navigation if prompted. This
requires the updated Host and its configured Google callback website. The Host
operator can add a manual username/password to the **same Google-linked
account** in Accounts, keeping Google and game data intact. An empty password is
supported but is less secure.

The unsigned-app warnings below apply to both apps. On macOS, open
`Traveller Tracker.app` rather than `Traveller Host.app` for the player client.

## For hosts: download Traveller Host

Traveller Host is a desktop app that runs the server and manages accounts, data,
backups and online access. Get the newest version from the
**[latest release](https://github.com/JohnJettsberg/travellertrack/releases/latest)**
and pick the file for your system:

| System | Recommended | Alternative |
|--------|-------------|-------------|
| Windows | [Installer (.exe)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.17/Traveller-Host-0.2.17-win-x64.exe) | [Portable (.zip)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.17/Traveller-Host-0.2.17-win-x64.zip) |
| macOS (Apple Silicon) | [Disk image (.dmg)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.17/Traveller-Host-0.2.17-mac-arm64.dmg) | [Zip](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.17/Traveller-Host-0.2.17-mac-arm64.zip) |
| Linux (x64) | [AppImage](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.17/Traveller-Host-0.2.17-linux-x86_64.AppImage) | [Archive (.tar.gz)](https://github.com/JohnJettsberg/travellertrack/releases/download/v0.2.17/Traveller-Host-0.2.17-linux-x64.tar.gz) |

These links are for version 0.2.17. Newer versions are always on the
**[latest release page](https://github.com/JohnJettsberg/travellertrack/releases/latest)**.

The apps are not code-signed, so your system will warn you the first time:

- **Windows:** SmartScreen → **More info** → **Run anyway**.
- **macOS:** the easiest way, with no security warnings, is to paste this into
  Terminal. Run it again to update:

  ```sh
  curl -fsSL "$(curl -fsSL https://api.github.com/repos/JohnJettsberg/travellertrack/releases/latest | grep -o 'https://[^"]*/Traveller-Host-[^"]*mac-arm64.zip')" -o /tmp/th.zip && ditto -x -k /tmp/th.zip /Applications && rm /tmp/th.zip && open "/Applications/Traveller Host.app"
  ```

  Or use the disk image: right-click the app → **Open**. If it says the app is
  "damaged", run `xattr -cr "/Applications/Traveller Host.app"` in Terminal.
- **Linux:** make the AppImage executable (`chmod +x`) and run it. Recent
  Ubuntu/Debian may need `sudo apt install libfuse2`.

### Getting started as a host

1. Open Traveller Host and click **Start server**.
2. Open **Accounts** and create your admin account, then accounts for your players.
3. **Same home network:** players open `http://YOUR-LAN-IP:8787` directly in their
   browser (the app shows the address). Do not use the GitHub website for this.
4. **Friends elsewhere:** open **Go Online** and click **Turn on online link**. You get
   a public `https://` link to send them. No router setup is needed; friends open the
   link, or paste it into the **Server URL** box on the GitHub website. Port forwarding
   (plain HTTP) is the alternative: friends must then use the **Open direct link**
   button that appears on the website's login page, or type the address into the
   browser themselves.
5. Keep the app open while your group plays. Use **Back up database** regularly.

The GitHub website is HTTPS, so it can only talk to an HTTPS server, which the
online link provides. Plain `http://` addresses can instead be entered in the
Traveller Tracker desktop app or opened directly in the browser.

## Data and legal

Your data stays on the host's computer. Bundled game data comes from openly
licensed sources (the Traveller SRD / OGL and community open data). This is an
unofficial fan project. Traveller is a trademark of its owners and this project
is not affiliated with Mongoose Publishing.
