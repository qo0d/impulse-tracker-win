```text
                                    ▄▄▄█▓▓▄▄
                              ▄▄▄███████▓▓▓▓▓▓▓▄▄▄
                        ▄▄▄█████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▄▄▄
                  ▄▄▄███████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▄▄▄
            ▄▄▄█████████████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▄▄▄
          ██████████████████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
          ██████████████████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
          ██████████████████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
          ██████████████████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
          ██████████████████████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
          █████████▓▓▓▓▓▒▒▓█████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒▓▓▓▓▓▓▓▓▓▓▓▓▓▓
          ██▓▓▓▓▓▓▓▒▒▒▒▒▒▒▓█████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▓▓▓▓▓▓▓
            ▀▀▀▀▀▒▒▒▓▓▒▒▒▓▓█████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▒▒▒▒▒▒▒▒▒▀▀▀▀
                     ▀▀▀▀▒▓█████████████▓▓▓▓▓▓▓▓▓▓▓▓▓▀▀▀▀▀
                           █████████████▓▓▓▓▓▓▓▓▓▓▓▓
                           █████████████▓▓▓▓▓▓▓▓▓▓▓▓
                           ███████████▓▓▓▓▓▓▓▓▓▓▓▓▓▓
                           ████▓▓▓▓▓▒▒▒▒▒▒▒▒▒▓▓▓▓▓▓▓
                           ▀▀▀▀▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▀▀▀▀
                                  ▀▀▀▀▒▒▒▀▀▀▀

                     ░ ▒ ▓    T E S S E R A . T V    ▓ ▒ ░

    ██████████ █████████ ▄███████  ▄███████  █████████ ████████▄  ▄▄██████
        ██     ██        ██        ██        ██        ██     ██ ▄█▀    ██
        ██     ██▄█████  ▀███████▄ ▀███████▄ ██▄█████  ██▄▄▄▄██▀ ██     ██
        ██     ██               ██        ██ ██        ██▀▀██▀   █████████
        ██     ▀████████ ████████▀ ████████▀ ▀████████ ██   ▀██▄ ██     ██

                         I M P U L S E   T R A C K E R
                     N A T I V E   W I N D O W S   P O R T

                               dYNAX / tessera.tv
```

# Impulse Tracker — Native Windows Port

A native Windows x64 port of Impulse Tracker, based on the original source
code by Jeffrey Lim. The DOS-era workflow and original tracker logic are
retained, with native Windows audio, MIDI and window handling.

Windows port by **dYNAX (qo0d)** — [tessera.tv](https://tessera.tv).

Current release: **v0.2.2**. See [CHANGELOG.md](CHANGELOG.md) for features
and limitations, and the repository's **Releases** page for downloadable builds.

```text
  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
 ▐██▓▒░▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ 01 / DOWNLOAD AND RUN ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀░▒▓██▌
  ▀▀───────────────────────────────────────────────────────────────────────▀▀
```

Open **Releases** on this repository's GitHub page and choose from **Assets**:

| Download | Contents |
| --- | --- |
| `impulse-tracker-windows-x64-v0.2.2.zip` | Application and documentation, without songs or samples. |
| `impulse-tracker-windows-x64-v0.2.2-full.zip` | The same application, two original example songs and the starter sound bank. |

Both editions use the same EXE. Verify either ZIP against `SHA256SUMS.txt`.
The downloadable application is in that ZIP; GitHub's automatically generated
“Source code” archives contain this repository's documentation.

1. Extract the entire ZIP to a writable folder.
2. Run `impulse-tracker.exe`. No Python or development tools are required.
3. Press **Ctrl+O** to open a module, **F5** to play and **F8** to stop.

The application saves its preferences and caches locally. See `START-HERE.txt`
in the ZIP for keyboard shortcuts and further instructions.

```text
  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
 ▐██▓▒░▀▀▀▀▀▀▀▀▀▀▀▀▀▀ 02 / FEATURES / WINDOWS PORT 0.2.2 ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀░▒▓██▌
  ▀▀───────────────────────────────────────────────────────────────────────▀▀
```

This release includes the features below; some original features remain incomplete.
Real-device Windows audio, input and MIDI validation is still in progress.

- Load IT, S3M, MOD, XM, MTM and 669 songs; save edited songs as IT.
- Edit patterns, samples and instruments, and play modules.
- Export stereo 16-bit / 44100 Hz WAV files.
- Use native Windows MIDI input/output and an adaptive tracker interface.
- Choose WASAPI, an installed ASIO driver, or waveOut in Playback Menu -> Driver Screen.
- Enable stereo-linked output peak protection without changing module volumes.

Known limitations include unsupported stereo samples inside IT songs,
incomplete original commands and formats, and reported audio crackle still
under investigation. External MIDI audio is not included in WAV exports.
Back up important modules before editing them with this version.

```text
  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
 ▐██▓▒░▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ 03 / EXAMPLE MODULES ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀░▒▓██▌
  ▀▀───────────────────────────────────────────────────────────────────────▀▀
```

The **Full edition** includes just two original Impulse Tracker examples:

- **Blue Flame** — Chris Jarvis (`CHRIS31B.IT`).
- **Drifting Onwards** — Jeffrey Lim (`JEFF93.IT`).

Open them from `songs/it214v5`. [SONG-CREDITS.md](SONG-CREDITS.md) records their
origin, hashes and rights information. They are not licensed under the starter
bank's CC0 dedication or the program's BSD license.

The Full edition also includes **Tessera Starter Sounds** in `samples/starter`:
24 drum files and 17 bass, synth, strings and keys instruments. These are original
synthesized timbres, not hardware or acoustic recordings. Some drum files share
PCM; the bank is not advertised as 41 unique sounds. See
[STARTER-SOUNDS.txt](STARTER-SOUNDS.txt) for loading instructions and CC0 credits.

The application-only edition contains neither music nor sample files.

```text
  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
 ▐██▓▒░▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ 04 / CREDITS AND LICENSE ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀░▒▓██▌
  ▀▀───────────────────────────────────────────────────────────────────────▀▀
```

Original Impulse Tracker: **Jeffrey Lim**.
Native Windows port: **dYNAX (qo0d)**.
Full scene credits and greetings are in [release.nfo](release.nfo).

The original code's BSD 3-Clause copyright, terms and disclaimer are preserved
in [LICENSE](LICENSE). See [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)
for upstream and asset information. This is an independent port.

This repository currently distributes the Windows application and its
documentation. The native port's source code is not included.

```text
  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
 ▐██▓▒░▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ 05 / REPORTING PROBLEMS ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀░▒▓██▌
  ▀▀───────────────────────────────────────────────────────────────────────▀▀
```

Use this repository's **Issues** tab. Include the build filename, Windows
version, audio/MIDI device, steps to reproduce and expected behavior.
If a module is required to reproduce the problem, share it only if you have
permission to do so.
