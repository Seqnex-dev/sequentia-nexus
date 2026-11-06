<p align="center">
  <img src="assets/logo/sequentia_nexus.png" alt="Sequentia Nexus" width="120">
</p>

<h1 align="center">Sequentia Nexus</h1>

<p align="center">
  Build a video processing workflow once, then run it on a whole folder of movies or TV series.<br>
  Extract, convert, fix subtitles, merge or encode, without typing a single command.
</p>

<p align="center">
  <img alt="Version" src="https://img.shields.io/badge/version-0.51.1-0e639c">
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0e639c">
  <img alt="Status" src="https://img.shields.io/badge/status-beta-d08a1e">
</p>

<p align="center">
  <img src="docs/images/main_dark.png" alt="Sequentia Nexus main window" width="900">
</p>

---

## What it does

Sequentia Nexus is a desktop app for people who prepare their own video library. You pick the
steps you need from a catalog, set them up once, and the app runs them in the right order on
every video in a folder. The result is a clean MKV with the audio and subtitles you want.

- **Read DVDs and Blu-rays** (`.iso` files, `VIDEO_TS` / `BDMV` folders, the drive of the PC)
  into MKV files without re-encoding: the main film or the episodes of a series are proposed,
  episodes named `Show - S02E01 - Episode title` (titles from TVmaze). Only discs without
  protection.
- **Transfer audio and subtitles**: the audio and the subtitles of one version of a film (a DVD,
  a 720p...) brought onto another version (the 1080p, the 4K): for example a dubbed language onto
  a film that has only the original one. Speed (PAL), delay and different cuts are found by
  comparing the two audio tracks; subtitles follow as text or as pictures (DVD, Blu-ray), in more
  languages if wanted; versions paired by title and year.
- **File information**: what a video contains (tracks, languages, HDR, 3D, fonts) and what your
  workflow will do with it, before you start; drag a video onto the window to see it.
- **Extract** the best audio track and all subtitles in your language, sorted into
  *forced*, *regular* and *SDH*; optionally **more audio languages** too, for example the
  original one next to the dubbed one, with their subtitles.
- **Convert the audio**: keep it as it is or convert it (AC3, E-AC3, AAC, FLAC, DTS, Opus,
  MP3), with 5.1 / 7.1 upmix and an optional even loudness (EBU R128) for every episode.
  Several files are converted at the same time.
- **Read image subtitles** from Blu-rays (`.sup`) and DVDs (`.idx/.sub`) and turn them into
  SRT text, with a smart correction that fixes the typical OCR mistakes.
- **Fix the subtitles**: clean tags and encoding errors, create a missing *regular* or
  *forced* subtitle, resync the timing, and add your own find-and-replace rules with a live
  preview on the real subtitles of your videos.
- **Merge** everything into an MKV, or **encode** the video (NVIDIA NVENC or CPU,
  H.264 / H.265). With two NVIDIA cards, two videos are encoded at the same time, and the
  CPU converts the audio while the cards encode.
- **Encode preview**: a piece of a video encoded with your settings, with the size and time
  expected for the whole video, the quality (VMAF) and a frame to compare with the original.
- **Clean up the picture** before the encode: automatic deinterlacing (only when the video
  needs it, also NTSC telecine), black bars cropped, noise reduction for old DVDs.
- **3D → 2D**: a 3D video (side by side or top and bottom) is recognised from its flag, its
  name and above all its picture, and comes out in 2D; a Blu-ray 3D gives the film in 2D.
- **Resolution and quality**: a maximum resolution (a 4K film becomes 1080p, never enlarged;
  resized on the video card when possible), constant quality (CRF, automatic by resolution) and
  two passes for the CPU encoders.
- **HDR videos**: kept as HDR in H.265 10 bit, or converted to SDR with natural colours
  (tone mapping on the video card) in H.264.
- **Burn subtitles into the video** (hardsub): SRT with a Blu-ray-like style, ASS with its own
  style and fonts, Blu-ray and DVD image subtitles as they are. The fonts of ASS subtitles
  stay in the final file; an episode that lacks one borrows it from the other episodes.
- **Change the aspect ratio** of the final files without re-encoding.
- **Upload the finished files to your NAS** (SFTP, FTPS or FTP), also from outside home,
  into the movies and series folders, with resume if the connection drops: several files at
  once, and each file as soon as it is ready, while the others are still encoding.
- **Movies and TV series** can have separate folders and separate settings: one workflow,
  two passes.
- **Pause and resume** a run, see the **time left** and the encode speed, put the PC to
  **sleep, hibernate it or shut it down when done**; the workflow runs at low priority, so the PC
  stays usable.
- **Updates**: the program tells you when a new version is out and downloads it for you
  (nothing installs by itself).
- **Queue**: several workflows, each with its own folders, run one after the other; all the
  checks are done at the start, then it runs unattended, every job with its own log.
- **Guide in 11 languages**, inside the program (Help → Documentation, F1: chapters, search,
  always up to date from the site) and at
  **[sequentianexus.com/guide](https://sequentianexus.com/guide/)**.
- **Presets**, a check before every run, a live log, a progress bar that moves while
  each file is worked on, a workflow list where every working step shows a turning arrow and
  each finished step a ✓ or ✗ (for movies and TV series separately), an optional notification on screen or on Telegram when the work is
  done, dark and light themes.
- **Eleven languages**: English, Italian, French, German, Spanish, Portuguese (Portugal),
  Portuguese (Brazil), Romanian, Russian, Turkish and Simplified Chinese. Each language is one file in `languages/`, so a new one can be
  added without touching the code.

## Screenshots

<table>
  <tr>
    <td width="50%"><img src="docs/images/main_light.png" alt="Light theme"><br><sub>Light theme: audio settings</sub></td>
    <td width="50%"><img src="docs/images/main_aspect_ratio.png" alt="Choose the files of a step"><br><sub>Choose which files a step applies to</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/images/rules.png" alt="Custom subtitle rules"><br><sub>Custom subtitle rules with a live preview</sub></td>
    <td width="50%"><img src="docs/images/prefs_ocr.png" alt="OCR preferences"><br><sub>OCR languages, downloaded with one click</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="docs/images/prefs_folders.png" alt="Folder preferences"><br><sub>Folders: one set for everything, or movies and series apart</sub></td>
    <td width="50%"><img src="docs/images/requirements.png" alt="System requirements"><br><sub>Requirements checked and installed for you</sub></td>
  </tr>
</table>

## Requirements

| | |
|---|---|
| **System** | Windows 10 or 11 (macOS and Linux are planned) |
| **FFmpeg** and **MKVToolNix** | Required. Installed from the app (*Settings → System Requirements*) |
| **Tesseract OCR** | Optional: only the image subtitle step needs it |
| **NVIDIA GPU** | Optional: only for NVENC encoding. The CPU encoders work everywhere |
| **License** | Beta testers receive a license key. One license works on one PC, and starting a workflow needs an internet connection |

FFmpeg, MKVToolNix and Tesseract are separate programs with their own licenses: the app
installs them with `winget` and calls them, it does not include them. The other components
inside the program are listed, with their licenses, in `THIRD-PARTY-NOTICES.txt` in the zip.

## Getting started

1. Download `SequentiaNexus-<version>-windows.zip` from the [Releases](../../releases) page and
   unpack it in a folder of your choice.
2. Double-click **`SequentiaNexus.exe`**. The program is not signed yet: if Windows shows
   *Windows protected your PC*, click **More info** → **Run anyway**.
3. The first time, the **System Requirements** window opens by itself: press
   **Install all missing**.
4. Get your free beta key at [sequentianexus.com/beta](https://sequentianexus.com/beta), then
   open **Settings → Preferences → License**, paste it and press **Activate**.
5. Open **Settings → Preferences → Folders** and choose the folder with your videos and the
   folder for the finished files.
6. Double-click the steps you want in the **Script catalog**, set them up in **Parameters**,
   and press **▶ Start workflow**. An internet connection is needed to start a workflow.

During the beta the program is free: get your personal key at
**[sequentianexus.com/beta](https://sequentianexus.com/beta)**.

The full guide is in **[docs/HOW_TO_USE.md](docs/HOW_TO_USE.md)**, and in 11 languages at
**[sequentianexus.com/guide](https://sequentianexus.com/guide/)**.

## Feedback

Sequentia Nexus is in beta. Bug reports and ideas are welcome in the
[Issues](../../issues) page. Please add the log of the run (*📋 Copy log*) and say which steps
were in the workflow. Issues are public: before pasting a log, remove what you do not want to
show, such as the address, port and user name of your server (*Upload to server* step).

## License

Copyright © 2026 Seqnex. All rights reserved. The beta is free for invited testers under the
[beta terms](BETA-TERMS.txt); the source code is not public.

Built with Qt for Python (PySide6, LGPL). Uses FFmpeg, MKVToolNix and Tesseract, installed
separately under their own licenses. OCR models: Tesseract `tessdata_best` (Apache 2.0).
Word frequencies: [FrequencyWords](https://github.com/hermitdave/FrequencyWords)
(OpenSubtitles).
