# homebrew-anubis

Homebrew tap for [Anubis OSS](https://github.com/uncSoft/anubis-oss) — local LLM benchmarking on Apple Silicon.

## Install

```bash
brew install --cask uncsoft/anubis/anubis-oss
```

Or, if you prefer to tap explicitly:

```bash
brew tap uncsoft/anubis
brew install --cask anubis-oss
```

## What you get

The native macOS app, signed and notarized by Apple. On first launch:

- Pick a backend (Ollama / LM Studio / MLX / Apple Intelligence)
- Pull a model — either browse the Ollama registry directly from the toolbar, or type a name
- Run a benchmark and optionally submit to the [community leaderboard](https://devpadapp.com/leaderboard.html)

In-app updates via Sparkle remain enabled — you'll be prompted for new versions as they ship. Or run `brew upgrade --cask anubis-oss` to update on your own schedule.

## Uninstall

```bash
brew uninstall --cask anubis-oss          # removes the .app
brew uninstall --cask --zap anubis-oss    # also removes Library/ data (history DB, Sparkle cache, prefs)
```

## Requirements

- macOS 15 (Sequoia) or later
- Apple Silicon (M1 or newer recommended; supported chips: M1–M5 family + A18 Pro)

## Source

The cask formula in `Casks/anubis-oss.rb` is generated from the [main repo](https://github.com/uncSoft/anubis-oss/blob/main/homebrew/anubis-oss.rb). Per-release bumps are handled by [`scripts/bump-cask.sh`](https://github.com/uncSoft/anubis-oss/blob/main/scripts/bump-cask.sh) — see [`homebrew/README.md`](https://github.com/uncSoft/anubis-oss/blob/main/homebrew/README.md) for the workflow.

## License

The cask formula is MIT. Anubis OSS itself is GPL-3.0.
