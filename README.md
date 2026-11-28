# Reywvo

hey, this is Reywvo (it used to be called Rewyvo, and Zenvio before that: same app, the name just changed). it's a free little clipping app for Windows that I made because I got tired of my clipper eating my RAM and CPU while I play.

you play like normal, something cool happens, you press **F8** and the last 60 seconds get saved as a video. that's basically it.

## download

**[⬇ Download Reywvo-Setup.exe](https://github.com/ipo461/zenvio-releases/releases/latest/download/Reywvo-Setup.exe)** (always the newest version) and run it. no account, no sign up, nothing.

Windows 10 or 11, 64-bit. more about it on the website: [reywvo.com](https://reywvo.com)

**"Windows protected your PC"?** click **More info → Run anyway**. Windows shows that for apps that aren't code-signed yet (signing costs money every year, and Reywvo is free). updates are still signed with my own key, and the app refuses any update that isn't.

once it's installed it updates itself. new versions download in the background, also while you're recording or playing, at low priority so it doesn't cost FPS. it never installs mid-game: only when you press "Update & restart" (you get a little "update ready" message) or when Windows starts. you can turn that off in settings if you don't want it.

## what it does

- saves the last 30 / 60 / 120 seconds when you hit your key (F8 by default, you can change it)
- plays a sound when the clip saved so you know it worked without tabbing out
- only records when you're actually in a game, not when you're on youtube or discord
- records game sound and your mic, and in the clip player you can mute or turn down each one (or split game / voice chat / music into their own tracks)
- cut and trim clips right in the player
- clip library with thumbnails, sorted by game
- star clips you want to keep
- "shrink" button that makes a clip small enough to send on discord
- **phone** button: watch and download your clips on your phone over your home wifi (nothing goes to the internet)
- storage limit (10 GB by default) so it doesn't fill up your drive. when it's full it deletes the oldest clip that isn't starred and tells you which one

## why I made it

the main thing I cared about is that it's light. I tested it against Medal in Rainbow Six Siege on my pc (Ryzen 5 3500X + RTX 3050, 1080p, same route, 3 runs each):

| | Reywvo | Medal |
|---|---|---|
| FPS lost while recording | **−6.5** | −7.5 |
| 1 % lows (stutters) | **93.9** | 92.0 |
| CPU | **2 %** | 4 % |
| graphics card video encoder | **7 %** | 15 % |
| RAM | **~180 MB** with the window closed (~365 MB open) | ~1,313 MB |

every clipper costs a few FPS because copying and encoding the screen isn't free, Reywvo just does it with less work. when you close the Reywvo window it fully closes, and only the small recorder stays in the tray. (the 180 MB figure is from my separate long recording tests with the window closed; during the benchmark runs the window was open.)

## good to know

- works with **NVIDIA, AMD and Intel** graphics cards (it uses the card's built-in video encoder). I've only been able to test on NVIDIA so far, so if something's off on AMD or Intel please send a problem report
- games in borderless or windowed mode work best. exclusive fullscreen might not
- your clips stay on your pc. Reywvo doesn't upload anything. it only goes online to check this page for updates (and download them), for a tiny anonymous once-a-day head count you can switch off, and when you send a problem report yourself

## something broke?

use **Report a problem** in the app (left sidebar, under Settings). you see exactly what gets sent before you click Send, and you can delete your report later. please **don't post your log files in public GitHub issues**: they can contain your folder names and which games and apps you ran.

no internet, or the app won't open at all? open an [issue](https://github.com/ipo461/zenvio-releases/issues) and describe what happened (no logs, nothing personal: issues are public).

## terms & privacy

by using Reywvo you agree to the [terms of use](https://reywvo.com/terms/). the [privacy policy](https://reywvo.com/privacy/) explains the little bit of data Reywvo ever handles (update checks, the anonymous head count, and problem reports you send yourself). questions or deleting a report: iposbots@proton.me

## credits

video recording uses [FFmpeg](https://ffmpeg.org) (LGPL), audio uses [NAudio](https://github.com/naudio/NAudio), icons are from [Lucide](https://lucide.dev). the app comes with THIRD-PARTY-NOTICES.txt and a `licenses` folder with the full licence texts (including every library inside FFmpeg); the complete FFmpeg source code is a free download (see THIRD-PARTY-NOTICES.txt).
