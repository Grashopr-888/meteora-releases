# Changelog

## 0.3.0 — 2026-11-06 · first public release (preview for ADC 2026)

The first version of Meteora anyone outside the project can try. macOS on Apple Silicon, VST3 and Standalone, free.

**The reverb**
- A stereo reverb computed from a model of Meteora, Greece, built from open data (Copernicus elevation and
  OpenStreetMap): echoes come off the modelled rock faces at their real distances and directions; air absorption
  after ISO 9613-1, with temperature, humidity, wind and inversion.
- Two virtual microphones you place anywhere in the valley or on the rocks, with polar patterns modelled after
  common studio microphones, aim and elevation; split, morph and spread blend modes.
- Faces: choose a rock face, resize it, make it breathe or flutter.
- A 3D site model on the panel shows the terrain, the microphones and the echo paths as they happen; an echo scope
  shows every echo and the tails.
- A patch row after the Buchla 200 series: random, function, follower and oscillator sources into any control.

**New in 0.3: a reverb that listens**
- A real-time listener hears attacks, density, brightness, pitch and noisiness; its LISTENER module in the patch
  row turns what it hears into cable sources for any control.
- The ALIVE guide, from subtle to drastic: LISTEN (suggests pot values and cables, moves nothing), SETTINGS (moves
  pots), PATCH (makes its own cables), ALIVE (both). LOCK, KEEP, A/B and RETURN keep you in charge; the guide never
  writes your host automation. MIRROR or COUNTER: the place follows or contrasts with your playing.
- The EXTREME lamp and the status line say when the plug-in leaves the physics.

**Also**
- 41 factory presets in groups (Places, Air, Faces, Shape, Mics, Patches, Alive, Utility); user presets.
- LEARN mode ("?") explains every control.
- Every control (106) is automatable.
- Panel themes: light, dark grey and dark.
- Tested before release: unit tests, pluginval at strictness 10, Steinberg's VST3 validator (47 of 47), address,
  thread and real-time sanitizers, and soak tests of the panel under load.

**Known limits** are listed in the README: Apple Silicon only, not notarised (one Terminal line), no AU or Windows
yet, the space bar in Live, and the guide's choices are first guesses.
