# Clipbot Studio (beta)

Turn streams, VODs and long videos into short clips **and** full YouTube videos, on your own computer.
Paste a Kick, Twitch or YouTube link, a Dropbox, Google Drive or WeTransfer link, or drop in any file.

## Download

**[Download Clipbot Studio](https://github.com/magicman007-code/clipping-bot-releases/raw/main/clipbot-beta.zip)**
(version 2.3.0) · Mac, Windows and Linux.

Already installed? Press **Update** in the top bar. Your projects, settings and your own edits are kept, and the update
waits for running jobs to finish. Reload the page once after updating.

## What it does

| | |
|---|---|
| **Auto-clip** | Finds the best moments in a stream (speech, reactions, chat spikes), scores them, and makes finished vertical clips with captions and a headline. Pick how many, or press **More clips**. |
| **Edit anything** | Click anything on the video to move, resize, duplicate or delete it. **Add** text, emoji or a **blur** (blur, pixelate or black box for faces, names or chat). Captions, fonts, framing, stream windows, cuts, undo. |
| **Make a YouTube video** | Turns a long stream into a 5–30 minute video: best stories in order, cold open, chapter cards, YouTube chapters and an end screen. Change, retime or reorder the parts, or open any part in the full editor, then rebuild. |
| **Thumbnails** | Big-creator style thumbnails from the real frame, with the person cut out and bold words, plus optional AI backgrounds. |
| **Publish and schedule** | Upload to YouTube (title, description, tags, thumbnail), post to TikTok (draft or direct), send to your phone with a QR code, or use a folder that Buffer or Later picks up. **Schedule posts** spreads clips over the coming days, for example 2 a day. |
| **Results** | Views for everything you post, new views in the last 24 hours, and what's working for you: which lengths, times and platforms get the most views. |
| **Track accounts** | Paste any YouTube, TikTok, Twitch or Kick profile to follow its followers and views, even accounts you haven't connected. Posts that match your clips are linked automatically. Instagram Reel views with your own token. |
| **Shorts from long videos** | One click turns each part of a long video into a vertical Short. |
| **Live** | Clips a stream while it's live, or watches a channel and clips every new VOD. Can make real Twitch clips. |
| **Learns** | Your ratings, edits, views and streamer notes ("lore") shape the next picks. Optional skills teach the AI your taste. |
| **Phone alerts** | Free push alerts (ntfy) when clips are ready, a video is built, a post goes up or something fails. |

**Simple mode** (the default) shows only what you need, with a 1-2-3-4 guide: Pick → Edit → Render → Post. **Pro**
shows every tool.

**New here?** Press **Open the demo project** on Home. A **Guide** opens beside it and walks you through 10 small steps
in plain words (watch a clip, change the headline, add text, blur, trim, render, make a YouTube video, post, see
results). **Show me** lights up the right button, and each step ticks itself off when you do it. Press **Guide** in the
top bar to bring it back any time.

## Install

**Mac**
1. Install [Homebrew](https://brew.sh) (paste the line it shows into Terminal, then run the "Next steps" lines it prints).
2. Unzip the download, then in Terminal: `cd ~/Downloads/clipbot` and `./install.sh`.
   It installs everything else itself, including Python 3.12 and the full ffmpeg that captions need. It ends with
   `"ready": true`.
3. Start it any time with `cd ~/Downloads/clipbot && ./start.sh`.

**Windows**
1. Install [Python 3.12](https://www.python.org/downloads/) and tick **"Add python.exe to PATH"**.
2. Unzip to a folder like `C:\clipbot` (not inside OneDrive).
3. Right-click `install.ps1` → **Run with PowerShell**. Start it any time by double-clicking `start.bat`.

**Linux:** unzip, then `./install.sh` and `./start.sh`.

The guide is `BETA_TESTING.md` inside the zip. Connecting YouTube, TikTok, Twitch, your own AI and phone alerts is
covered step by step in `CONNECT.md`.

## Your data and responsibility

- Everything runs on your computer. Your videos and projects stay there unless you upload, post or share them.
- On first launch you choose whether to share **anonymous learning reports** (off unless you turn it on) and whether to
  use the **free built-in AI**, which sends clip text to a public service. You can change both any time in Settings.
- You're responsible for the footage, people and content you clip and post: you need the rights or permission to use
  them. The full terms are in `TERMS.md` and are shown on first launch.

## What's new

**2.3.0**
- **Guide for beginners:** a 10-step, hands-on checklist on the demo project. Plain words, a "Show me" button that
  highlights where to click, and steps that tick themselves off. The tester guide starts with a no-experience quick
  start and a few words explained.
- **Track accounts** in Results: followers, recent views, new views since yesterday and top posts for any YouTube,
  TikTok, Twitch or Kick profile, checked every 6 hours. Your clips are found on those accounts automatically.
- **Instagram views** through Instagram's official API with your own token (steps in `CONNECT.md`). Clipbot renews the
  token weekly so it doesn't expire.
- Fixed: when a background job failed (a render, an upload, a YouTube edit), the screen could keep waiting instead of
  showing what went wrong. It now shows the error straight away.

**2.2.0**
- **Schedule posts:** spread rendered clips over the coming days on YouTube (it publishes them even if your computer is
  off), as TikTok drafts, or to your posting folder. Cancel or retry them in Results.
- **Results:** total views, last 24 hours, best clip, a trend line for every post, and "What's working" patterns
  (for example "Clips under 20 s get 2.9× the views"), compared fairly by views per day.
- **Fix a word everywhere:** double-click a misheard word or name and it's fixed throughout the video, and remembered so
  future transcriptions get it right.
- Home and Results keep the left rail usable.

**2.1.0**
- Phone alerts are smarter: posts link straight to the video, failures are flagged, and several renders arrive as one
  alert. Setup is one button plus a QR code.
- The first-launch screen now asks whether to share learning reports and whether to use the free AI.
- One-click demo project (a 2-minute stream) to try every feature, including long YouTube videos.
- Clearer empty screens, and an updated guide and tour (demo, phone alerts, Simple and Pro).

**2.0.0**
- Fits every screen from small laptops to big monitors. One toolbar above the video.
- Edit on the video: drag, resize from the corner, nudge with the arrow keys, Ctrl+D to duplicate, Delete to remove.
  Blur, pixelate or black out anything. The final video matches the preview.
- Long YouTube videos: edit any part in the full editor, publish to YouTube, make Shorts, add an end screen.
- Simple and Pro modes, TikTok posting, Twitch clips, terms screen and security hardening.
