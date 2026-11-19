# Rewyvo

hey, this is Rewyvo (it was called Zenvio until november 2026, same app). it's a little clipping app for Windows that I made because I got tired of my clipper eating my RAM and CPU while I play.

you play like normal, something cool happens, you press **F8** and the last 60 seconds get saved as a video. that's basically it.

## download

grab the **Setup.exe** from the [Releases](https://github.com/ipo461/zenvio-releases/releases/latest) page and run it. no account, no sign up, nothing.

once it's installed it updates itself. when there's a new version you get a little "update ready" message and you click it. you can turn that off in settings if you don't want it.

## what it does

- saves the last 30 / 60 / 120 seconds when you hit your key (F8 by default, you can change it)
- plays a sound when the clip saved so you know it worked without tabbing out
- only records when you're actually in a game, not when you're on youtube or discord
- records game sound and your mic, and in the clip player you can mute or turn down each one
- clip library with thumbnails, sorted by game
- star clips you want to keep
- "shrink" button that makes a clip small enough to send on discord
- storage limit (10 GB by default) so it doesn't fill up your drive. when it's full it deletes the oldest clip that isn't starred and tells you which one

## why I made it

the main thing I cared about is that it's light. on my pc (Ryzen 5 3500X + RTX 3050) it used way less CPU and RAM than the clipper I was using before (about 3.5x less CPU and 9x less RAM in my tests). FPS was about the same, because grabbing the screen costs the same for every app that does it. when you close the Rewyvo window it fully closes, and only the small recorder stays in the tray.

## good to know

- **NVIDIA graphics card only for now** (it uses the card's built-in video encoder). AMD and Intel might come later
- Windows 10 or 11, 64-bit
- games in borderless or windowed mode work best. exclusive fullscreen might not
- your clips stay on your pc. Rewyvo doesn't upload anything. it only goes online to check this page for updates, and when you send a problem report yourself

## something broke?

use **Report a problem** in the app (left sidebar, under Settings). you see exactly what gets sent before you click Send, and you can delete your report later. please **don't post your log files in public GitHub issues**: they can contain your folder names and which games and apps you ran.

no internet, or the app won't open at all? open an [issue](https://github.com/ipo461/zenvio-releases/issues) and describe what happened (no logs, nothing personal: issues are public).

## terms & privacy

by using Rewyvo you agree to the [terms of use](https://github.com/ipo461/zenvio-releases/blob/main/TERMS.md). the [privacy policy](https://github.com/ipo461/zenvio-releases/blob/main/PRIVACY.md) explains the little bit of data Rewyvo ever handles (update checks, and problem reports you send yourself). questions or deleting a report: iposbots@proton.me

## credits

video recording uses [FFmpeg](https://ffmpeg.org) (LGPL), audio uses [NAudio](https://github.com/naudio/NAudio), icons are from [Lucide](https://lucide.dev). the app comes with THIRD-PARTY-NOTICES.txt and a `licenses` folder with the full licence texts (including every library inside FFmpeg); the complete FFmpeg source code is a free download (see THIRD-PARTY-NOTICES.txt).
