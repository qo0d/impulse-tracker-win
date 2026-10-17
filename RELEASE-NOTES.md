# Impulse Tracker Windows Port v0.2.0 — WASAPI and ASIO

Native Windows x64 port by dYNAX (qo0d), based on Jeffrey Lim's Impulse Tracker
source code. This release combines the audio backend work with 0.1.2's
output peak protection and MIDI integration.

Download `impulse-tracker-windows-x64-v0.2.0.zip`, extract the entire archive
and run `impulse-tracker.exe`. No installation or Python is required.
`SHA256SUMS.txt` provides the archive's checksum.

Open Esc -> Playback Menu -> Driver Screen to choose:

- WASAPI shared event-driven output (default). Supported low-latency engine
  periods are requested through IAudioClient3; otherwise standard shared mode
  is used. Windows handles continuous sample-rate conversion when needed.
- ASIO using an installed 64-bit driver, with buffer selection and its control
  panel. No ASIO driver is installed by this package.
- waveOut as the explicit compatibility option or fallback after an open error.

Opening audio settings stops playback. The chosen device opens on the next
play; the window title reports the actual backend and any fallback reason.
Backend/device/buffer and peak-protection preferences are saved together;
older ITDESKTOP.CFG files remain readable.
Driver Screen now uses the IT font/palette with mouse and keyboard selection.
Buffers range from Auto/64 to 4096 frames; standard WASAPI shared mode also
receives the requested capacity. The actual size can be larger. After playback,
the screen and local log show the actual stream, observed queue starvation and
render/service timing. These counters do not measure every source of crackle.

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

Output peak protection is still enabled by default for playback, audition and
Render WAV. Alt+Space -> Output peak protection restores the original output.
It adds 64 frames (1.45 ms at 44100 Hz); its -1 dBFS sample ceiling is not a
true-peak guarantee. Song/sample/instrument volumes are unchanged.

The ZIP includes eight unchanged CC BY 4.0 example modules with credits and
license links. Native port source, local settings and personal files are excluded.

Targeted native/model tests, a mock-driver ASIO contract test, and the Windows
cross-build passed. A Windows run confirms the F5 crash fix and WASAPI startup
on Realtek headphones. Load-related crackle remains under investigation; the
latest buffer/UI changes, ASIO devices/panels, default-device changes and
Yamaha MIDI latency still need hardware testing. A smaller buffer is not a
measured end-to-end latency result.

Some original features remain incomplete; stereo samples inside IT songs are
unsupported. WAV export cannot record audio from external MIDI instruments.
Back up important modules. See CHANGELOG.md for changes and limitations.
