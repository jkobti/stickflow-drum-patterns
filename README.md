
# stickflow-patterns

A curated open-source library of drum patterns for drummers of all levels,
exported from [StickFlow](https://www.stickflow.app). A web-based drum
practice tool with notation rendering, audio playback, and tempo tracking.

The library currently contains patterns across three categories: grooves,
fills, and rudiments. Each pattern is provided as a MusicXML file with a
JSON metadata sidecar.

---

## Library Structure

patterns are organized by category:

```
grooves/
  {pattern-id}.musicxml
  {pattern-id}.json
fills/
  {pattern-id}.musicxml
  {pattern-id}.json
rudiments/
  {pattern-id}.musicxml
  {pattern-id}.json
patterns.json
export-info.json
```

`patterns.json` is a full manifest of all patterns with their metadata.
`export-info.json` contains the export date, pattern count, and source info.

---

## Pattern Metadata Format

Each `.json` sidecar follows this schema:

```json
{
  "id": "uuid",
  "title": "Basic Rock Groove",
  "category": "groove",
  "description": "A straight 4/4 rock groove with a backbeat on snare.",
  "difficulty": "beginner",
  "tags": ["rock", "4/4", "hihat"],
  "default_bpm": 90,
  "time_signature": "4/4",
  "bar_count": 2,
  "subdivision": 16,
  "exported_at": "2026-06-02T07:00:00Z"
}
```

**Difficulty values:** `beginner`, `intermediate`, `advanced`

**Category values:** `groove`, `fill`, `rudiment`

---

## Using the Patterns

The MusicXML files follow the standard unpitched percussion format and can
be opened in MuseScore, Sibelius, Finale, or any MusicXML-compatible tool.
They can also be parsed programmatically using libraries such as
[music21](https://web.mit.edu/music21/) (Python) or
[OpenSheetMusicDisplay](https://github.com/opensheetmusicdisplay/opensheetmusicdisplay)
(JavaScript).

---

## Export Date

See `export-info.json` for the latest export date and full export metadata.

---

## License

The patterns in this library are released under the
[Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
You are free to use, share, and adapt them for any purpose, including
commercial use, as long as you give appropriate credit to StickFlow.

---

## Contributing

This repository is an automatic export of the StickFlow pattern library.
Patterns and metadata are managed in StickFlow and exported here as a
read-only snapshot.

If you are interested in helping with the library, contact
joseph@stickflow.app and we can find the best way to work together.

---

## About StickFlow

StickFlow is a web-based drum practice tool built for drummers of all levels.
It features a pattern library with notation rendering, a smart player with
tempo tracking, a looper with YouTube and MP3 support, and multiplayer
practice games.

Visit [stickflow.app](https://www.stickflow.app) to try it.
