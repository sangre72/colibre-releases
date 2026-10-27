# THIRD_PARTY_NOTICES

Colibre is proprietary, commercial software (see `LICENSE` / `LICENSE.ko`). It is **not** released under the GPL or any other open-source license.
The Colibre installer also contains third-party open-source programs and libraries. They are governed by their own licenses, not by the Colibre Terms, and the Terms do not limit your rights under those licenses.
Full license texts ship inside the installed program (`licenses\` folder: `README.md`, `npm\`, `rust\`, `vendor\`, `source\`, plus `THIRD-PARTY-NOTICES.txt`).
Questions: support@colibre.app

## 1. Executables shipped with the installer

| Component | License | Source / notes |
|---|---|---|
| FFmpeg (`ffmpeg.exe`, `ffprobe.exe`) n8.1.3-17-gc389840894 + 1 patch (`libavutil/hwcontext_d3d11va.c`) | LGPL-3.0-or-later (modified build) | Complete corresponding source (original revision, patch, build recipe): https://github.com/sangre72/ffmpeg/tree/n8.1.3-17-d3d11fix |
| Node.js v24.12.0 (`node.exe`, Windows x64) | MIT (plus bundled library notices: https://github.com/nodejs/node/blob/v24.12.0/LICENSE) | https://nodejs.org |
| yt-dlp (`yt-dlp.exe`) | Unlicense (public domain). The Windows executable is a PyInstaller bundle that includes Python (PSF License) and dependency packages, among them mutagen (GPL-2.0-or-later) | https://github.com/yt-dlp/yt-dlp |
| ViGEmBus driver | BSD-3-Clause | `licenses\ViGEmBus-LICENSE.txt` |
| Colibre engine, tray program and shim programs | Colibre proprietary license; bundled Rust crates are listed in `licenses\rust\README.md` | not distributed as source |

## 2. Obligations we honor

- **FFmpeg (LGPL-3.0-or-later, modified).** FFmpeg is run as a separate command-line program and is not linked into Colibre. Built from FFmpeg c389840894 plus one patch with the BtbN FFmpeg-Builds win64-lgpl-8.1 configuration (`--enable-version3`; no `--enable-gpl`, no `--enable-nonfree`). The LGPL-3.0 and GPL-3.0 texts are included (`licenses\vendor\ffmpeg-LGPL-3.0.txt`, `ffmpeg-GPL-3.0.txt`). The complete corresponding source is public at the repository above and will stay public for as long as installers containing this build are distributed. You may replace `bin\ffmpeg.exe` and `bin\ffprobe.exe` with your own build.
- **mutagen 1.48.1 inside yt-dlp.exe (GPL-2.0-or-later).** yt-dlp.exe is shipped unmodified, as a separate program. As required by GPL-2.0 section 3(a), the mutagen source for that build is included in the installer (`licenses\source\mutagen-1.48.1.tar.gz`).
- **mediabunny (MPL-2.0).** A bundled player file contains mediabunny code and we patch that file. The patch (the source of the modified file) is published in `licenses\source\` (MPL-2.0 section 3.2).
- **sharp / libvips (LGPL-3.0-or-later).** Shipped as a separate, replaceable DLL.
- **node-forge (BSD-3-Clause OR GPL-2.0).** Used under BSD-3-Clause (notice only).
- **Rust crates in the engine.** Permissive licenses only (MIT, Apache-2.0, BSD, ISC, Unicode-3.0, Zlib, CDLA-Permissive-2.0 and similar). Texts in `licenses\rust\`.
- **caniuse-lite (CC-BY-4.0).** Attribution: data from Can I use (https://caniuse.com), Alexis Deveria.
- **Geist and Geist Mono fonts (SIL OFL-1.1).** The OFL text ships with the fonts (`licenses\vendor\geist-font-OFL-1.1.txt`). https://github.com/vercel/geist-font

Further notices (for example the installer builder and machine-learning runtime and model licenses) are in `licenses\vendor\`. The complete package list (name, version, license, repository, license-text file) is in `licenses\README.md`, generated from the app (Next.js) and the HTTPS front (`installer/tls-front`) production dependencies.

## 3. Data and service attributions

- **MusicBrainz**: album metadata (core data CC0 1.0). https://musicbrainz.org, MetaBrainz Foundation. Requests are kept to at most one per second with a contact address in the User-Agent.
- **Cover Art Archive**: album art. Copyright in the artwork belongs to each rights holder. https://coverartarchive.org (MetaBrainz and Internet Archive).
- **LRCLIB**: lyrics (including timed .lrc). Copyright in lyrics belongs to each rights holder. https://lrclib.net
- **Stereophile**: one sound-tuning data set was transcribed as numbers from Fig. 4 (in-room 1/6-octave spatially averaged response measured by John Atkinson) of the November 2024 Stereophile measurements of the Avantgarde Duo SD iTRON G3 active loudspeaker. The figure itself is not included. https://www.stereophile.com/content/avantgarde-duo-sd-itron-g3-active-loudspeaker-measurements
- **Measurement method**: room-response measurement follows A. Farina's exponential sine sweep method (AES 108, 2000; AES 122, 2007).
- **Browser HRTF**: spatial audio uses the browser's built-in Web Audio HRTF (PannerNode "HRTF"). Colibre does not ship HRTF data.

## 4. Optional tools installed separately (not distributed with Colibre)

| Component | License | Notes |
|---|---|---|
| Apollo (code and official checkpoint) and PyTorch | CC BY-SA 4.0 (Apollo), BSD-3-Clause (PyTorch) | Optional feature "Advanced Audio Restore" (AI high-frequency restoration), off by default. The user installs these tools; they are not included in the Colibre installer. Colibre only runs them as a separate process. Source: Kai Li, Yi Luo, "Apollo: Band-sequence Modeling for High-Quality Audio Restoration" (2024), https://github.com/JusperLee/Apollo |

## Trademarks

FFmpeg is a trademark of Fabrice Bellard, originator of the FFmpeg project. Colibre is not affiliated with or endorsed by the FFmpeg project.
