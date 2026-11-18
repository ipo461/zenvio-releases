# Zenvio

hey, this is Zenvio. it's a little clipping app for Windows that I made because I got tired of my clipper eating my RAM and CPU while I play.

you play like normal, something cool happens, you press **F8** and the last 60 seconds get saved as a video. that's basically it.

## download

grab **ZenvioSetup.exe** from the [Releases](https://github.com/ipo461/zenvio-releases/releases/latest) page and run it. no account, no sign up, nothing.

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

the main thing I cared about is that it's light. on my pc (Ryzen 5 3500X + RTX 3050) it used way less CPU and RAM than the clipper I was using before (about 3.5x less CPU and 9x less RAM in my tests). FPS was about the same, because grabbing the screen costs the same for every app that does it. when you close the Zenvio window it fully closes, and only the small recorder stays in the tray.

## good to know

- **NVIDIA graphics card only for now** (it uses the card's built-in video encoder). AMD and Intel might come later
- Windows 10 or 11, 64-bit
- games in borderless or windowed mode work best. exclusive fullscreen might not
- your clips stay on your pc. Zenvio doesn't upload anything. the only time it goes online is to check this page for updates

## something broke?

open an [issue](https://github.com/ipo461/zenvio-releases/issues) and tell me what happened. if you can, add your log file (Zenvio → Settings → Troubleshooting → Open log folder).

## credits

video recording uses [FFmpeg](https://ffmpeg.org) (LGPL), audio uses [NAudio](https://github.com/naudio/NAudio), icons are from [Lucide](https://lucide.dev). the full licence texts come with the app in THIRD-PARTY-NOTICES.txt.
