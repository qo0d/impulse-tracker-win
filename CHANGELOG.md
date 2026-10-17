# Changelog

Versions here refer to the native Windows port, independently of the original
Impulse Tracker 2.14 version. This entry describes the first release package; GitHub publication is a separate step.

## 0.1.0 — First Windows release (packaged 2026-10-18)

### Included

- Native Windows x64 application based on Jeffrey Lim's Impulse Tracker source.
- IT, S3M, MOD, XM, MTM and 669 loading; pattern, sample and instrument editors;
  playback and saving edited songs as IT.
- Stereo 16-bit / 44100 Hz WAV export of the song's internal audio.
- Windows MIDI input/output, chord audition and live recording.
- Adaptive interface, mouse wheel navigation, draggable controls and Help.
- Nine unchanged CC BY 4.0 example modules, with composer credits, source
  links and file hashes in SONG-CREDITS.md.

### Audio and usability work included in this release

- Independent audio refill and direct MIDI-note delivery to the audio worker.
- Shorter PCM render blocks and less document-copying work under the audio lock.
- Short voice-boundary declick tails, a brief fade on Stop and raw sample-loop
  release handling. These changes do not establish that all crackle is fixed.
- Port version and credits aligned with the Done button on Help pages.

### Known limitations

- The original feature set is not fully implemented.
- Stereo samples inside IT songs are unsupported.
- WASAPI and ASIO are not included. The waveOut queue is about 35 ms;
  end-to-end hardware latency has not been measured.
- Reported audio crackle remains under investigation. Real Windows device
  checks, including MIDI hardware and background playback, remain outstanding.
- WAV export does not capture audio from external MIDI instruments.
- The public package contains binaries and documentation, not native port source.

### Verification

Targeted native/model tests and the Windows cross-build passed. Package
contents and checksums are verified; these are not real Windows device tests.
