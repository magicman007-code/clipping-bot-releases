# Clipbot (beta)

Turns streams, VODs and any video into short-form clips, with a full editor, captions, live clipping and
streamer-aware moment finding. Paste a Kick or Twitch VOD, a YouTube video, or a Dropbox / Google Drive /
WeTransfer link, or drop in any file. Moments where chat explodes rank higher, it can watch channels and clip every
new VOD, you can plug in your own AI or scoring software, and it learns from the clips you keep. Runs on your own
computer.

## Download

**[Download the latest version](https://github.com/magicman007-code/clipping-bot-releases/raw/main/clipbot-beta.zip)**
(version 1.8.7).

## Install

**Mac**
1. Install [Homebrew](https://brew.sh) (paste the line it shows into Terminal, then run the "Next steps" lines it prints).
2. Unzip the download, then in Terminal: `cd ~/Downloads/clipbot` and `./install.sh`
   It installs everything else itself, including Python 3.12 and the full ffmpeg (`ffmpeg-full`) that captions need.
   It ends with `"ready": true`.
3. Start it any time with `cd ~/Downloads/clipbot && ./start.sh`

**Windows**
1. Install [Python 3.12](https://www.python.org/downloads/) and tick **"Add python.exe to PATH"**.
2. Unzip to a folder like `C:\clipbot` (not inside OneDrive).
3. Right-click `install.ps1` -> **Run with PowerShell**. Start it any time by double-clicking `start.bat`.

The first time, a 1-minute tour walks you through the editor. Full guide: `BETA_TESTING.md` inside the zip.

## Updates

Clipbot checks this repository for new versions and shows an **Update** button in the top bar. Your projects and
settings are kept.
