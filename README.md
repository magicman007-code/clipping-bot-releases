# Clipbot Studio (beta)

Turn streams, VODs and long videos into short clips **and** full YouTube videos, on your own computer.
Paste a Kick, Twitch or YouTube link, a Dropbox, Google Drive or WeTransfer link, or drop in any file.

## Download

**[Download Clipbot Studio](https://github.com/magicman007-code/clipping-bot-releases/raw/main/clipbot-beta.zip)**
(version 2.5.1) · Mac, Windows and Linux.

Already installed? Press **Update** in the top bar. Your projects, settings and your own edits are kept, and the update
waits for running jobs to finish. Reload the page once after updating.

## What it does

| | |
|---|---|
| **Auto-clip** | Finds the best moments in a stream (speech, reactions, chat spikes), scores them, and makes finished vertical clips with captions and a headline. Pick how many, or press **More clips**. |
| **Follows who's talking** | A speaker-detection model watches each face and listens to the audio, and the vertical crop follows whoever is talking. When everyone fits, everyone stays in frame; when it can't tell, it shows both instead of guessing. |
| **Edit anything** | Click anything on the video to move, resize, duplicate or delete it. **Add** text, emoji or a **blur** (blur, pixelate or black box for faces, names or chat). Captions, fonts, framing, stream windows, cuts, undo. |
| **Make a YouTube video** | Turns a long stream into a 5–30 minute video: best stories in order, cold open, chapter cards, YouTube chapters and an end screen. Change, retime or reorder the parts, or open any part in the full editor, then rebuild. |
| **Thumbnails** | Big-creator style thumbnails from the real frame, with the person cut out and bold words, plus optional AI backgrounds. |
| **Publish and schedule** | Upload to YouTube (title, description, tags, thumbnail), post to TikTok (draft or direct), send to your phone with a QR code, or use a folder that Buffer or Later picks up. **Schedule posts** spreads clips over the coming days, for example 2 a day. |
| **Tell a clip what to change** | Type "cut the first 4 seconds", "follow the guy on the left", "fix the caption that says X, it should say Y" or "tighten this to the punchline". It changes that one clip, re-renders it, says what it did, and Undo takes it back. |
| **Checked, not just rendered** | Every clip reports its caption error rate (bar: 8%, or you approve), how much of the talking shows the speaker, and the footage's true resolution. Every clip also comes as a 1920x1080 landscape version. |
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

**2.5.1**
- Captions ease out once a phrase is finished. When the speaker pauses, the line stays readable for a moment, then
  fades away (and shrinks a touch in the Pro style) instead of sitting on screen through the pause. Fast talking
  still swaps lines instantly. The editor preview shows the same thing.

**2.5.0**: picks that hear and see the moment
- **Hears the room:** a sound model picks out laughter, cheering and applause on the stream, measured against that
  stream's own background. Tested on real recordings: it catches 80% of laughs with 1% false alarms. Under talking
  and crowd noise, a second with laughter outranks one without 93% of the time.
- **Sees reactions** in the best moments: a look into the camera, a double take, a side look, a face dropping into
  shock, disgust or a big laugh. Each face is compared with its own resting look, and a talking mouth isn't mistaken
  for shock (about one false beat per minute of calm talking).
- **Chat counts only when it's busy.** A small streamer's quiet chat no longer drives picks; what happens on stream
  does.
- **Faster renders** with your computer's video encoder (Apple, NVIDIA or Intel), falling back automatically if it
  doesn't work.
- The download is bigger (about 42 MB) because the sound and face models are included; nothing is sent anywhere.

**2.4.0**: fixes from a live IRL Kick test
- **The crop follows who's talking.** A speaker-detection model (Light-ASD) checks each face against the voice. On
  test footage with known speakers, the person talking is on screen 91% of the time, up from 77%, and the wrong
  person is picked 2.5% of the time, down from 13%. Unsure stretches show both people.
- **Captions:** speech that used to vanish is back. A repeated phrase could wipe out up to 30 seconds of captions,
  and Whisper could silently skip part of a window; both are fixed. Lines the model isn't sure of are left out
  instead of shown wrong. Each clip shows its real caption error rate, checked against a separate transcription;
  over 8%, it isn't done until you fix or approve the captions. Captions also stay clear of every face in the shot.
- **True 1080p:** live recording used to take 720p; now live and downloads take the best version up to 1080p and log
  what they got. The top bar shows the footage's real resolution and turns red under 1080p.
- **Landscape:** every final render also makes a 1920x1080 version.
- **Better picks:** a clip must have a payoff (a laugh, reaction, reveal or chat spike) to score above 5/10. Clips
  end on the payoff, 15-25 s is preferred, dead air and cut-off endings cost points, and the best three are marked
  Top 3.
- **Prompt box on every clip** (top of the Clip tab).
- **Hardening:** saved files survive crashes and damage (a damaged project opens and restores its last good clip
  list), empty folder paths are refused, the scheduler skips broken entries, and failed background jobs show their
  error instead of waiting forever.

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
