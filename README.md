# video-director-skills

Collection of Skills for Video Direction Agents.

## Available Skills

| Skill | Description | Prompt Example | Location | Reference |
| :--- | :--- | :--- | :--- | :--- |
| **`manim-skill`** | Create mathematical animations and 3Blue1Brown-style videos with Manim Community Edition, TTS voiceover, and synced subtitles. | `"Create an animation explaining the Pythagorean theorem."` | [.agents/skills/manim-skill](.agents/skills/manim-skill/SKILL.md) | [Yusuke710/manim-skill](https://github.com/Yusuke710/manim-skill) |

## Requirements

| Skill | Requirements |
| :--- | :--- |
| **`manim-skill`** | Python 3.10+, `manim>=0.18`, `ffmpeg`, `cairo`, `pkg-config`, LaTeX (`mactex-no-gui`), `kokoro>=0.9.4` & `soundfile` (for local TTS voiceover) |

## Installation

### `manim-skill`

```bash
# System libraries (macOS)
brew install cairo pkg-config ffmpeg
brew install --cask mactex-no-gui   # LaTeX — required for Tex/MathTex text rendering

# Python packages — Manim + local Kokoro voiceover (no API key needed)
uv sync --project .agents/skills/manim-skill
```

## Usage Notes

- **Sandbox**: The `local/` subdirectory is configured to be ignored by git. Use this directory as a sandbox to place your project files, or ask the agent to create its own files there.
- **Kokoro TTS Voices**: Browse and preview available Kokoro voices in the [Kokoro Voice Gallery](https://rewind.ai/voices/) (pass `--voice <name>` to `tts-generate.py`, default: `am_michael`).
- **3Blue1Brown Video Codebase**: Reference [3b1b/videos](https://github.com/3b1b/videos) for the original 3Blue1Brown animation codebase and scene patterns.
