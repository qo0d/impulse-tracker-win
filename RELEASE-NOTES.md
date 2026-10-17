# Impulse Tracker Windows Port v0.1.0 — First release

The first release of the native Windows x64 port by dYNAX (qo0d), based on
Jeffrey Lim's original Impulse Tracker source code.
Version 0.1.0 of the Windows port. See `CHANGELOG.md`
for the included features and known limitations.

Download `impulse-tracker-windows-x64-v0.1.0.zip`, extract the entire
archive and run `impulse-tracker.exe`. No installation or Python is required.
`SHA256SUMS.txt` provides the archive's checksum.

The package contains the Windows application, startup instructions, license
notices, scene NFO and nine attributed CC BY 4.0 modules in `songs/cc-by-4.0`.
The native port's source code is not included.

Implemented functionality includes module loading, pattern/sample/instrument
editing, playback, IT saving, WAV export and native MIDI integration.

This build routes MIDI notes directly to the audio worker, renders shorter
PCM blocks and reduces document synchronization work under the audio lock.
Help now aligns the port version and credits with the Done button.
The waveOut queue remains about 35 ms; end-to-end hardware latency has not
been measured. WASAPI and ASIO are not included in this build.

Known limitations: some original features remain incomplete, stereo samples
inside IT songs are unsupported, and real-device Windows audio/input/MIDI
validation remains outstanding. Reported audio crackle is still under
investigation. Back up important modules before editing.

The Windows EXE is cross-compiled. Native/model tests and package checks
do not replace real Windows device testing.
