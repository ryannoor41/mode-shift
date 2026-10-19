# Mode Shift Studio

**Eight original songs in the styles of modern pop, R&B, Afrobeats and trap, and a way to slide each one through all seven musical modes.**

Created by **Ryan Noorbakhsh**.

**Live app:** https://USERNAME.github.io/mode-shift/

## The styles

| Style | Genre | Home mode | Influences |
|---|---|---|---|
| Daydream Pop | Bedroom pop | Lydian | Clairo, Steve Lacy, Rex Orange County |
| Afro Sunshine | Afrobeats | Ionian | Wizkid, Burna Boy, Tems |
| Velvet Neo-Soul | R&B ballad | Ionian | Daniel Caesar, Giveon, H.E.R. |
| Retro Funk-Soul | Funk and soul revival | Mixolydian | Silk Sonic, Bruno Mars, Anderson .Paak |
| Late-Night Alt-R&B | Alternative R&B | Dorian | SZA, Brent Faiyaz, Frank Ocean |
| Neon Synth-Pop | 80s-style synth-pop | Aeolian | The Weeknd, Dua Lipa, Harry Styles |
| Dark Whisper Pop | Minimal dark pop | Phrygian | Billie Eilish and FINNEAS, Lorde |
| Villain Trap | Trap | Locrian | Metro Boomin, Travis Scott, Future |

Every song is an original composition written for this project in the general production style associated with the artists listed: tempo, groove, instruments, chord colors and melodic habits. No melodies, lyrics, samples or recordings from those artists are used, and the project is not affiliated with or endorsed by them.

## Features

- **Full arrangements:** intro, two verses, two hooks and an outro, with drums, bass, chords, a topline and a texture layer (pads, arpeggios, vinyl crackle).
- **Mode ladder:** the seven modes ordered from brightest (Lydian) to darkest (Locrian). Pick any rung and the whole arrangement re-maps instantly, even mid-song. The sky behind the music goes from noon to night.
- **Live multi-track view:** topline piano roll, chord names, bass line and drum grid with a playhead. Notes that moved from the style's home mode are highlighted and marked ♭ or ♯, and chords that changed are outlined.
- **Write a new topline:** a seeded melody generator builds a motif, answers it, repeats it over the next chord and lands on a chord tone, using rhythm and register rules tuned to each style. The seed is stored in the URL so melodies can be shared.
- **Mixer:** mute, solo and volume for each track, with live level meters.
- **Controls:** key, tempo, swing, loop the current section, and jump to any section on the timeline.
- **Theory panel:** the mode's notes, step pattern, comparison with major, the diatonic chords with Roman numerals (the playing chord lights up), and a keyboard that shows the scale and the notes being played.
- **Shareable links**, for example `#late-night-rnb/phrygian/2612`.

## How it works

Every chord, bass line and melody is stored as scale-degree numbers instead of fixed pitches. To play a song in a mode, the app looks up each degree in that mode's interval pattern and adds the result to the chosen key. Chords are built by stacking thirds from the current mode, then named automatically (so a V9 becomes v9, or a major 9th becomes a m7(♭9), depending on the mode).

Sound is synthesized live with the Web Audio API, using no samples:

- FM electric piano, piano and bells
- Formant-filtered sawtooth "vocal" leads with scoops and delayed vibrato
- Gliding, saturated 808s, sub and synth basses
- Drums made from pitched sine sweeps and filtered noise
- Detuned saw pads, a choir pad, plucked arpeggios
- Shared reverb and tempo-synced delay, sidechain-style ducking, tape wobble and tremolo

A look-ahead scheduler on a 16th-note grid (with adjustable swing) keeps timing tight while letting mode, key, tempo and mix change live.

Everything is one self-contained `index.html`: plain HTML, CSS and JavaScript with no build step and no libraries.

## Run it locally

Open `index.html` in a modern browser and press Play.

## License

Copyright (c) 2026 Ryan Noorbakhsh. All rights reserved. See [LICENSE](LICENSE).
