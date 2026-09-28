# garyjeong/homebrew-tap

Personal [Homebrew](https://brew.sh) tap.

## Add the tap

```bash
brew tap garyjeong/tap
```

(`homebrew-tap` on GitHub is installed as the short name `tap`.)

## Casks

### AI Platform Monitor

Menu bar app for AI platform usage %, status health and Mac resource charts (floating widget included).

```bash
brew tap garyjeong/tap
brew install --cask gary-ai-platform-monitor
```

- Source: [garyjeong/gary-ai-platform-monitor](https://github.com/garyjeong/gary-ai-platform-monitor)
- Releases: [v0.6.0](https://github.com/garyjeong/gary-ai-platform-monitor/releases/tag/v0.6.0)
- Requires macOS 14 (Sonoma) or later
- **Apple Silicon (arm64) only** for the published DMG
- Build is **unsigned** — first launch may need right-click → **Open**

Upgrade:

```bash
brew update
brew upgrade --cask gary-ai-platform-monitor
```

Uninstall:

```bash
brew uninstall --cask gary-ai-platform-monitor
```

## Maintainers

When cutting a new app release:

1. Tag the app repo (`vX.Y.Z`) and wait for the Release workflow DMG  
2. Get the asset's sha256 (GitHub computes it; no download needed):

   ```bash
   gh api repos/garyjeong/gary-ai-platform-monitor/releases/tags/vX.Y.Z --jq '.assets[].digest'
   ```

3. Update `Casks/gary-ai-platform-monitor.rb` (`version` + `sha256`)  
4. Commit and push this tap

## License

Cask formulas are public domain style as usual for Homebrew.  
Application binaries follow the MIT license of [gary-ai-platform-monitor](https://github.com/garyjeong/gary-ai-platform-monitor).
