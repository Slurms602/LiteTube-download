# Third-party programs bundled with LiteTube

LiteTube runs these as separate programs (in `tools\`); they are unchanged copies of their official releases, pinned
by version and SHA-256 in `build.ps1`.

| Program | Version | Licence | Source |
|---|---|---|---|
| mpv (player) | 0.42.0, x86_64-pc-windows-msvc | GPL-2.0-or-later (this build includes GPL parts) | https://github.com/mpv-player/mpv |
| yt-dlp | 2026.10.26 (updates itself) | The Unlicense; the Windows executable bundles Python and other libraries under their own licences | https://github.com/yt-dlp/yt-dlp |
| Deno | 2.9.8 | MIT | https://github.com/denoland/deno |

ffmpeg is not bundled: the first download fetches it (FFmpeg's LGPL "shared" Windows build from
https://github.com/BtbN/FFmpeg-Builds, LGPL-2.1-or-later; source at https://ffmpeg.org) into %LOCALAPPDATA%\LiteTube\ffmpeg.

LiteTube also asks two services while it runs (nothing of them is bundled): SponsorBlock (https://sponsor.ajay.app,
its data is CC BY-NC-SA 4.0, by its contributors) for the parts of videos to skip, and YouTube's public channel feeds
for the followed channels.

mpv's source code for the bundled version is available at https://github.com/mpv-player/mpv/releases/tag/v0.42.0.

LiteTube's own code is MIT-licensed (LICENSE). Parts of it (the JSON reader, the log, the player's IPC client and the
process job handling) are adapted from LiteView (MIT, Copyright (c) 2026 Deezy) and LiteView Enhanced.
