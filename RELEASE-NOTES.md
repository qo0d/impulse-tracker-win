# Impulse Tracker Windows Port v0.2.2 — Clear Windows port credit

Small presentation update to v0.2.1, by dYNAX (qo0d).

Choose one of two downloads:

- `impulse-tracker-windows-x64-v0.2.2.zip`: application only, without music or samples.
- `impulse-tracker-windows-x64-v0.2.2-full.zip`: the same EXE, two original example
  songs (Blue Flame and Drifting Onwards) and Tessera Starter Sounds.

Extract the entire archive and run `impulse-tracker.exe`.
No installation or Python is required.
Verify the archive against `SHA256SUMS.txt`.

## Changes

- The original Jeffrey Lim copyright text is preserved and shifted left.
- Win port by dYNAX appears separately on the right in a muted color, with
  a clear gap. Detailed author information and tessera.tv remain in Help.
- The in-app Windows port version is now 0.2.2.
- Refreshed Tessera NFO artwork and acknowledgements, in UTF-8 and CP437.

The cursor-step wheel navigation and menu improvements from v0.2.1 are retained.
UI regression tests, the Windows x64 cross-build and optimized audio adapter
ABI checks passed. These checks do not replace a run on Windows hardware.

## Audio and compatibility

Audio, MIDI and file formats are unchanged by this update. WASAPI shared,
ASIO and waveOut remain available. Load-related crackle is still under
investigation; real ASIO devices and Yamaha latency require hardware validation.

Some original features remain incomplete; stereo samples inside IT songs are
unsupported. WAV export cannot record audio from external MIDI instruments.
Back up important modules before editing them. See CHANGELOG.md for history.

The Full bank contains 41 preset files (24 ITS drums, 17 ITI instruments) under
CC0. These are synthesized timbres, not recordings of branded hardware or
acoustic instruments; some drum PCM is shared between presets.
The two original songs have separate rights; see SONG-CREDITS.md.
The eight-track CC BY selection is no longer bundled.

Native port source, local settings, personal files, API/MCP and Modern UI are
excluded. The bank's developer showcase and WAV audition are not bundled.
