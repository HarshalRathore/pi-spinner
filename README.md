# @dustydonkey/pi-spinner

> Smooth working spinner with shimmering verbs for [Pi](https://pi.dev) — inspired by Claude Code.

Replace Pi's default Braille spinner with customizable frame presets, rotating status verbs, and a gentle per-character shimmer effect that pauses when the agent is idle.

## Demo

<video src="https://raw.githubusercontent.com/HarshalRathore/pi-spinner/main/assets/demo.mp4" controls width="100%"></video>

---

## Install

```bash
pi install npm:@dustydonkey/pi-spinner
```

Or project-local:

```bash
pi install npm:@dustydonkey/pi-spinner -l
```

Then `/reload`.

---

## Features

- **6 frame presets** — Claude Code's star sequence, Braille, pulse, dot, star, or none
- **5 verb presets** — 187 Claude Code verbs, short, technical, fun, or custom
- **Shimmer effect** — Gentle per-character color sweep across the verb text
- **Idle-aware** — Automatically pauses shimmer when waiting for sub-agents or user input (no glitchy re-rendering)
- **Fully configurable** via `/spinner` and `/verbs` slash commands
- **Settings persist** to `.pi/settings.json`

---

## Usage

### Slash commands

| Command | Description |
|---------|-------------|
| `/spinner` | Show current preset |
| `/spinner claude` | Use Claude Code star frames |
| `/spinner braille` | Use Braille dot frames |
| `/spinner pulse` | Use pulse animation |
| `/spinner dot` | Static dot |
| `/spinner star` | Star burst frames |
| `/spinner none` | Hide spinner |
| `/spinner frames ·,✢,✳,✶,✻,✽` | Custom frames |
| `/spinner interval 150` | Set frame interval (ms) |
| `/verbs` | Show current verb preset |
| `/verbs claude` | 187 Claude Code verbs |
| `/verbs short` | 6 focused verbs |
| `/verbs technical` | 12 dev verbs |
| `/verbs fun` | 23 whimsical verbs |
| `/verbs none` | Disable verbs |
| `/verbs add reading,typing` | Append custom verbs |
| `/verbs replace foo,bar` | Replace all verbs |

### Settings

Saved to `.pi/settings.json` under the `workingSpinner` key:

```json
{
  "workingSpinner": {
    "frames": "claude",
    "frameIntervalMs": 150,
    "verbs": "claude",
    "verbRotationIntervalMs": 3000,
    "showCompletionVerb": true,
    "completionVerbDurationMs": 2000
  }
}
```

---

## Why this exists

Pi's default Braille spinner is functional but plain. This extension adds:

1. **Visual polish** — Customizable frames make waiting feel intentional
2. **Context** — Rotating verbs ("Analyzing...", "Typing...", "Planning...") hint at what the agent is doing
3. **Delight** — The gentle shimmer gives the terminal life without being distracting
4. **Performance** — Shimmer pauses during idle states so sub-agent execution doesn't cause terminal flicker

---

## Gallery

Find it on [pi.dev/packages](https://pi.dev/packages?name=spinner).

---

## License

MIT
