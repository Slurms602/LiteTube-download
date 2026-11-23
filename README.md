# LiteTube (download)

LiteTube is a light Windows app for watching YouTube: a queue of the videos you pick, each playing in its own small
window that sleeps (no player running) until you click it. Where you stopped is remembered, and the next start
continues there. No browser, no ads, no account needed.

**Download:** the newest installer is on the [Releases page](../../releases/latest) (`LiteTube-Setup-<version>.exe`).

## Install

1. Download `LiteTube-Setup-<version>.exe` from the [newest release](../../releases/latest) and run it.
   It installs for your Windows account only (no administrator rights needed).
2. The installer is not code-signed yet, so Windows may show "Windows protected your PC": click **More info**, then
   **Run anyway**.
3. Windows 10 or 11, 64-bit. Everything it needs is included (the mpv player, yt-dlp and Deno).

Your queue and settings are kept in `%APPDATA%\LiteTube`; installing a newer version over an older one keeps them.
Uninstall from Windows' *Apps* settings like any program.

## Using it

- Copy a YouTube link anywhere (or several): it is added to the queue. Ctrl+V in LiteTube or dropping links works too.
- Double-click a video to play it. Videos LiteTube has looked up ahead (marked *starts at once*) start in a second or two.
- Paste a channel's link (youtube.com/@name) to see its videos; *Follow* puts its new videos under the *New* tab.
- Right-click a video for more: favorite, download (best quality, 4K, 1080p... or sound only), browse its channel.
- In a video window: Space pause, Left/Right 5 s, F fullscreen, A sound only, C subtitles, S favorite, N next video.
- SponsorBlock skips sponsor segments (press U to watch one anyway).

## If a video does not play

YouTube sometimes asks some networks (often VPNs) to "confirm you're not a bot". Try without the VPN, or in LiteTube's
menu choose *yt-dlp > Use my browser's YouTube cookies* (Firefox works best).

LiteTube's log is in `%APPDATA%\LiteTube\logs\litetube.log`.

## Licences

LiteTube is MIT-licensed (LICENSE). It bundles mpv (GPL), yt-dlp (Unlicense) and Deno (MIT) unchanged; see
THIRD_PARTY_NOTICES.md for their sources.
