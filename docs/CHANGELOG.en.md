# Changelog

[Русский](../CHANGELOG.md) · [Українська](CHANGELOG.uk.md) · [English](CHANGELOG.en.md) · [Deutsch](CHANGELOG.de.md)

## 0.2.0 — July 27, 2026

- added an antivirus-style file protection center with quick, selective, full, and multi-drive scans;
- implemented SHA-256, format detection, static analysis, YARA-X, ReversingLabs, and curated Signature-Base rules;
- added MalwareBazaar, URLhaus, and VirusTotal file reputation without uploading file contents;
- added SQLite caching and journal, pause/resume, and download/removable-drive monitoring;
- implemented encrypted quarantine, SHA-256-verified restore, and manageable hash exclusions;
- threat actions now require quarantine, skip, or exclude confirmation by default;
- added system context-menu scanning and safe updates that stop the app and service;
- redesigned the file UI as a professional protection center in four languages.

## 0.1.5 — July 26, 2026

- fixed corrupted Russian and Ukrainian text in the installer;
- forced the NSIS script input encoding to UTF-8;
- verified the compiled installer window through Windows UI Automation.

## 0.1.4 — July 26, 2026

- added an installer option to choose NyaaGuard as the HTTP/HTTPS default app;
- opens the relevant Windows Default Apps page after registration;
- added a “Set as default” button to Settings;
- localized the feature in all four interface languages.

## 0.1.3 — July 26, 2026

- added an installer language selector for Russian, Ukrainian, English, and German;
- localized custom pages, errors, and uninstallation;
- remembered the selected language for later updates;
- added branded installer iconography and a large logo;
- expanded the tracking-parameter cleanup documentation.

## 0.1.2 — July 26, 2026

- reduced spacing between entries in custom domain lists;
- added an official API-key link to the VirusTotal settings page;
- updated the interface and Russian, Ukrainian, English, and German translations;
- synchronized the Windows installer, portable build, and Debian package.

## 0.1.1 — July 26, 2026

- made donation addresses selectable and copyable through the context menu;
- removed non-working copy buttons;
- moved update checks to the GitHub Contents API.

## 0.1.0 — July 26, 2026

- first public Windows x64 and Debian/Ubuntu amd64 release;
- URL cleanup, local threat databases, custom lists, redirect inspection, and response-code checks;
- optional VirusTotal checks, tray operation, proxy support, and four interface languages.
