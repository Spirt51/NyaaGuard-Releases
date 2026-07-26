# NyaaGuard Releases

Official update metadata and binary releases for NyaaGuard.

This repository intentionally contains no application source code. Published
releases will include:

- Windows and Linux packages;
- macOS packages when platform support is ready;
- SHA-256 checksums and detached signatures;
- release notes;
- `update-manifest.json` used by the application updater.

The NyaaGuard source repository remains private.

Each populated channel in `update-manifest.json` uses this structure:

```json
{
  "version": "0.2.0",
  "publishedAt": "2026-07-26T00:00:00Z",
  "notesUrl": "https://github.com/Spirt51/NyaaGuard-Releases/releases/tag/v0.2.0",
  "artifacts": [
    {
      "rid": "win-x64",
      "url": "https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/NyaaGuard-Setup-0.2.0-win-x64.exe",
      "sha256": "<lowercase SHA-256>",
      "fileName": "NyaaGuard-Setup-0.2.0-win-x64.exe"
    }
  ]
}
```
Official NyaaLink releases and update metadata. Source code is maintained privately.
