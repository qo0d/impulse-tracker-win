# Impulse Tracker — Native Windows Port v0.3.0

> **Two interface styles: press Ctrl+Shift+G to switch between Classic and HQ (Hi-Res). Try both!**

Release candidate — built and packaged locally; final interactive Windows validation is pending.

Impulse Tracker's keyboard-driven workflow with native Windows audio and MIDI,
a choice of Classic and HQ interfaces, and an adaptive layout.
Windows port by **dYNAX (qo0d)** — [tessera.tv](https://tessera.tv).

## What's new

- Press **Ctrl+Shift+G** to switch between Classic and HQ interface styles.
- Music-reactive Demo scenes and an integrated portrait ANSI/NFO viewer.
- Windows help grouped by task, separate from the original tracker help.
- Sample-page typography and layout corrections, and instrument note-map mouse
  column selection with a visible editing cursor.

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

## Public package

One Windows x64 archive contains the application, documentation and two example
modules. No standalone sound bank is included. Classic, HQ, Demo and NFO are included. AI assistance
and the advanced waveform editor/chopper are excluded from the public edition;
normal sample loading, audition and parameter controls remain.

Extract the entire archive and run `impulse-tracker.exe`.
No installation or Python is required. Download: `impulse-tracker-windows-x64-v0.3.0.zip`.
Verify it against the accompanying `SHA256SUMS.txt`.

## Compatibility and validation

WASAPI shared, ASIO and waveOut remain available. External MIDI audio is not
captured by WAV export. Some original features and formats remain incomplete.
The public Windows cross-build and native UI, instrument, ITI and Demo/NFO
tests passed. Archive integrity and exclusions were checked. Interactive Windows
and hardware audio/MIDI validation remain pending;
this release does not claim to resolve every reported audio crackle.

Example songs retain their separate rights; see [SONG-CREDITS.md](SONG-CREDITS.md).
No standalone instruments or drum bank are bundled.

## In development

**Impulse Tracker Studio — an unofficial edition by dYNAX, currently in development.**
Studio is being developed separately with AI assistance and advanced sample
editing. It is not included in this public release. No release date is announced.
