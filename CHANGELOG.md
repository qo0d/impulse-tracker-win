# Changelog

Versions here refer to the native Windows port, independently of the original
Impulse Tracker 2.14 version. Entries describe prepared release packages;
GitHub publication is a separate step.

## 0.2.0 — WASAPI and ASIO (packaged 2026-10-18)

### Added / Fixed

- Select WASAPI shared, installed ASIO drivers, or waveOut in Playback Menu ->
  Driver Screen. WASAPI is preferred; failed opens fall back to waveOut with
  an explanation. Device choice, buffer target and protection settings persist.
- Request supported WASAPI engine periods through IAudioClient3; retain
  standard shared-mode compatibility and delegate rate conversion to Windows.
- ASIO adapter supports stereo int16/int24/int32/float32 driver planes, driver
  buffer constraints, callbacks, reset notification and the driver control panel.
- Keep backend open/render/position/close on one audio worker thread. Callback
  output does not allocate or wait on a mutex. Account for ASIO output latency;
  injected silence does not falsely advance the song/MIDI clock.
- Preserve all 0.1.2 peak protection, MIDI and rendering fixes. Fix settings
  migration, dialog control coordinates, partial-open cleanup and large-buffer
  waveform bounds during integration.
- Fix a Windows F5 startup crash caused by optimized COM interface calls;
  verify the actual optimized Windows adapter objects separately from mocks.
  Retain a local startup/crash log for diagnosis; normal audio blocks do not log.
- Restyle Driver Screen with the tracker font/palette and clickable buffer
  choices from Auto/64 through 4096 frames. Pass the requested capacity to the
  standard WASAPI shared fallback instead of silently ignoring the choice.
- Show the actual last stream, observed queue starvation, render cost and
  longest service gap. Exclude intentional drains from starvation counts.
- Limit audio-driven visual notifications to about 30 Hz without throttling
  rendering or MIDI. Avoid generating a full visual snapshot just to test for
  active voices; let laptop media/volume keys pass directly to Windows.
- Keep normal/maximized window placement across Alt+Enter; add mouse controls
  to restore/minimize from fullscreen.
- Add Alt/Shift + wheel channel scrolling and Ctrl + wheel adaptive column
  widths (14/11/8 cells), with every note/instrument/volume/effect field retained.
- Display Russian filesystem names in browsers without translating the path
  to DOS. Read/delete the selected native file, independently of the embedded
  8.3 filename. Original module metadata encoding remains unchanged.
- Add a separately selectable Windows Port Help section (Tab or click), and
  move Driver Screen [Exclusive] to the bottom of Playback Menu; Shift+F5 opens
  it directly. The badge identifies a port feature, not WASAPI exclusive mode.
- Remove Cortanosis Invading from the bundled selection at the user's request;
  retain eight attributed modules, including Shuffle (XM).

Native/model tests and mock-driver checks passed. A real Windows log and user
run confirm WASAPI starts on Realtek headphones after the F5 crash fix.
The user reports improved initial piano playback, but crackles under desktop
load remain unresolved. The latest buffer/UI changes, real ASIO and Yamaha
latency still require Windows hardware validation.

## 0.1.2 — Output peak protection (packaged 2026-10-18)

### Added / Fixed

- Output peak protection for songs, audition and Render WAV, enabled by
  default and switchable through Alt+Space. A wide master sum preserves peaks
  before PCM16 conversion. Stereo-linked limiting reduces overload without
  editing module or instrument volumes and without automatic make-up gain.
- The limiter adds 64 frames (1.45 ms at 44100 Hz); external MIDI timestamps
  include this delay. Its -1 dBFS ceiling is sample-peak, not true-peak.
  Disable protection to retain the original output behavior.
- Renamed the file-menu command to Render WAV and fixed Right Alt+Enter
  (including AltGr) fullscreen switching before page-specific key handlers.

The waveOut device queue and existing hardware-test limitations remain.
Protection does not repair damaged samples, loop discontinuities or device
underruns, and is not a claim that all reported crackle is eliminated.

## 0.1.1 — Filtered sample playback fix (packaged 2026-10-18)

### Fixed

- Fixed the filter-gain regression introduced by short PCM blocks in 0.1.0.
  After the first block, filtered voices incorrectly approached half volume
  until the next gain update. Their effective gain now persists across blocks.
- Added a regression comparing sustained filtered and unfiltered voices with
  whole-block and 128-frame rendering. Original low-level mixer kernels remain
  unchanged. This does not claim all previously reported crackle is resolved.

## 0.1.0 — First Windows release (packaged 2026-10-18)

### Included

- Native Windows x64 application based on Jeffrey Lim's Impulse Tracker source.
- IT, S3M, MOD, XM, MTM and 669 loading; pattern, sample and instrument editors;
  playback and saving edited songs as IT.
- Stereo 16-bit / 44100 Hz WAV export of the song's internal audio.
- Windows MIDI input/output, chord audition and live recording.
- Adaptive interface, mouse wheel navigation, draggable controls and Help.
- CC BY 4.0 example modules, with composer credits, source
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
