# Impulse Tracker — Native Windows Port

A native Windows x64 port of Impulse Tracker, based on the original source
code by Jeffrey Lim. The DOS-era workflow and original tracker logic are
retained, with native Windows audio, MIDI and window handling.

Windows port by **dYNAX (qo0d)** — [tessera.tv](https://tessera.tv).

First release: **v0.1.0**. See [CHANGELOG.md](CHANGELOG.md) for features
and limitations, and the repository's **Releases** page for downloadable builds.

## Download and run

Open **Releases** on this repository's GitHub page and download
`impulse-tracker-windows-x64-v0.1.0.zip` from **Assets**.
The downloadable application is in that ZIP; GitHub's automatically generated
“Source code” archives contain this repository's documentation.

1. Extract the entire ZIP to a writable folder.
2. Run `impulse-tracker.exe`. No Python or development tools are required.
3. Press **Ctrl+O** to open a module, **F5** to play and **F8** to stop.

The application saves its preferences and caches locally. See `START-HERE.txt`
in the ZIP for keyboard shortcuts and further instructions.

## Windows Port 0.1.0

This first release includes the features below; some original features remain incomplete.
Real-device Windows audio, input and MIDI validation is still in progress.

- Load IT, S3M, MOD, XM, MTM and 669 songs; save edited songs as IT.
- Edit patterns, samples and instruments, and play modules.
- Export stereo 16-bit / 44100 Hz WAV files.
- Use native Windows MIDI input/output and an adaptive tracker interface.

Known limitations include unsupported stereo samples inside IT songs,
incomplete original commands and formats, and reported audio crackle still
under investigation. External MIDI audio is not included in WAV exports.
Back up important modules before editing them with this version.

## Example modules

The Windows ZIP includes nine tracker modules from the CC BY 4.0 selection,
with music by Djego Flochs, Pip Malt, KuroFurtex, congusbongus and Andreas Viklund.
Open them from `songs/cc-by-4.0`.

[SONG-CREDITS.md](SONG-CREDITS.md) lists each track, composer, source page,
license link and original file hash. The same notice is included beside the
unmodified modules. Their music is licensed separately from the program.

## Credits and license

Original Impulse Tracker: **Jeffrey Lim**.
Native Windows port: **dYNAX (qo0d)**.
Full scene credits and greetings are in [release.nfo](release.nfo).

The original code's BSD 3-Clause copyright, terms and disclaimer are preserved
in [LICENSE](LICENSE). See [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)
for upstream and asset information. This is an independent port.

This repository currently distributes the Windows application and its
documentation. The native port's source code is not included.

## Reporting problems

Use this repository's **Issues** tab. Include the build filename, Windows
version, audio/MIDI device, steps to reproduce and expected behavior.
If a module is required to reproduce the problem, share it only if you have
permission to do so.
