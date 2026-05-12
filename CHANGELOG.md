# Changelog

## 1.0.0 (2026-05-12)

### Features
- 6 frame presets: `claude`, `braille`, `pulse`, `dot`, `star`, `none`
- 5 verb presets: `claude` (187 verbs), `short`, `technical`, `fun`, `none`
- Per-character shimmer color sweep across verb text
- Idle-aware shimmer: pauses when agent is not streaming (prevents terminal flicker during sub-agent execution)
- Configurable via `/spinner` and `/verbs` slash commands
- Settings persist to `.pi/settings.json`
- Completion verb on agent end (e.g. "Done!")

### Technical
- Uses `ctx.isIdle()` guard to skip `setWorkingMessage` calls during idle states
- Shimmer interval: 200ms (gentle, not aggressive)
- Verb rotation: 3000ms
- No build step — TypeScript loaded directly via jiti
