# garyjeong/homebrew-tap

Personal [Homebrew](https://brew.sh) tap.

## Add the tap

```bash
brew tap garyjeong/tap
```

(`homebrew-tap` on GitHub is installed as the short name `tap`.)

## Casks

### AI Platform Monitor

Menu bar app for AI platform usage % and status health.

```bash
brew tap garyjeong/tap
brew install --cask gary-ai-platform-monitor
```

- Source: [garyjeong/gary-ai-platform-monitor](https://github.com/garyjeong/gary-ai-platform-monitor)
- Releases: [v0.3.0](https://github.com/garyjeong/gary-ai-platform-monitor/releases/tag/v0.3.0)
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
2. Download the asset and hash it:

   ```bash
   gh release download vX.Y.Z -R garyjeong/gary-ai-platform-monitor -p '*.dmg'
   shasum -a 256 AI-Platform-Monitor-*.dmg
   ```

3. Update `Casks/gary-ai-platform-monitor.rb` (`version` + `sha256`)  
4. Commit and push this tap

## License

Cask formulas are public domain style as usual for Homebrew.  
Application binaries follow the MIT license of [gary-ai-platform-monitor](https://github.com/garyjeong/gary-ai-platform-monitor).
