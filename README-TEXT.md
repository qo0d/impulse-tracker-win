# Impulse Tracker — Native Windows Port

> **Two interface styles: press Ctrl+Shift+G to switch between Classic and HQ (Hi-Res). Try both!**

A native Windows x64 port of Impulse Tracker, based on the original source
code by Jeffrey Lim. The DOS-era workflow and original tracker logic are
retained, with native Windows audio, MIDI and window handling.

Windows port by **dYNAX (qo0d)** — [tessera.tv](https://tessera.tv).

Release in preparation: **v0.3.0**. See [CHANGELOG.md](CHANGELOG.md) for
changes and [RELEASE-NOTES.md](RELEASE-NOTES.md) for the release draft.
This documentation does not announce an available download yet.

## DOWNLOAD AND RUN

The planned public Windows x64 package contains the application, documentation,
example modules. No standalone sound bank is bundled. One public package is planned;
there is no Lite edition for this release.

The public build retains Classic and HQ interfaces, Demo and the NFO viewer.
AI assistance and the advanced waveform editor/chopper are not part of this
package. Ordinary sample loading, audition and parameter controls remain.
Prepared archive: `impulse-tracker-windows-x64-v0.3.0.zip`.
Check the accompanying `SHA256SUMS.txt`. Interactive Windows validation is pending.

1. Extract the entire ZIP to a writable folder.
2. Run `impulse-tracker.exe`. No Python or development tools are required.
3. Press **Ctrl+O** to open a module, **F5** to play and **F8** to stop.

The application saves its preferences and caches locally. See `START-HERE.txt`
in the ZIP for keyboard shortcuts and further instructions.

## FEATURES / WINDOWS PORT 0.3.0

The planned release includes the features below; some original features remain incomplete.
Real-device Windows audio, input and MIDI validation is still in progress.

- Load IT, S3M, MOD, XM, MTM and 669 songs; save edited songs as IT.
- Edit patterns and instrument mappings; load, audition and configure samples.
- Press **Ctrl+Shift+G** to switch between Classic and HQ interfaces with adaptive layouts.
- View music-reactive Demo scenes and the portrait ANSI/NFO artwork.
- Export stereo 16-bit / 44100 Hz WAV files.
- Use native Windows MIDI input/output and an adaptive tracker interface.
- Choose WASAPI, an installed ASIO driver, or waveOut in Playback Menu -> Driver Screen.
- Enable stereo-linked output peak protection without changing module volumes.

Known limitations include unsupported stereo samples inside IT songs,
incomplete original commands and formats, and reported audio crackle still
under investigation. External MIDI audio is not included in WAV exports.
Back up important modules before editing them with this version.

## Native Windows audio and WAV rendering

- **WASAPI shared** — native Windows playback through the system audio engine.
- **ASIO** — use an installed ASIO driver, its supported buffer sizes and control
  panel. Actual latency depends on the device and driver.
- **waveOut** — an alternative Windows output backend and compatibility fallback.
- **Interpolation:** Nearest (no interpolation), Linear, Cubic and Sinc8.
  Choose a playback character in **Playback Menu > Driver Screen** (Shift+F5).
- **Boundary declick** and **output peak protection** are separately selectable.
- **LUFS-S loudness metering and output peak meters.**
- **File Menu > Render WAV** exports stereo 16-bit / 44.1 kHz audio offline.
  It uses the module's Mix Volume, selected interpolation, boundary declick and
  peak protection settings. The master slider changes that module Mix Volume,
  so its setting is included in the render. Windows/device volume is not included.
  External MIDI instrument audio is not captured.

The original tracker workflow and musical playback logic are retained, with
additional output options for Windows. This is not a promise of bit-identical
DOS output or universally better sound. The original IT already supported
interpolation and disk writing, including cubic-spline disk output; the Windows
port offers its own selectable resampling implementation, including Sinc8.

## Why no bundled sample bank?

The experimental synthesized starter bank did not meet the sound-quality standard
we want for this release, so it has been left out. The package includes example
songs with their embedded sounds. Loading your own samples and instruments remains
available; no separate sound-bank edition is offered.

## EXAMPLE MODULES

The planned public package includes two original Impulse Tracker examples:

- **Blue Flame** — Chris Jarvis (`CHRIS31B.IT`).
- **Drifting Onwards** — Jeffrey Lim (`JEFF93.IT`).

Open them from `songs/it214v5`. [SONG-CREDITS.md](SONG-CREDITS.md) records their
origin, hashes and rights information. They are not licensed under the starter
bank's CC0 dedication or the program's BSD license.

## CREDITS AND LICENSE

Original Impulse Tracker: **Jeffrey Lim**.
Native Windows port: **dYNAX (qo0d)**.
Full scene credits and greetings are in [release.nfo](release.nfo).

The original code's BSD 3-Clause copyright, terms and disclaimer are preserved
in [LICENSE](LICENSE). See [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)
for upstream and asset information. This is an independent port.

This repository currently distributes the Windows application and its
documentation. The native port's source code is not included.

## REPORTING PROBLEMS

Use this repository's **Issues** tab. Include the build filename, Windows
version, audio/MIDI device, steps to reproduce and expected behavior.
If a module is required to reproduce the problem, share it only if you have
permission to do so.
