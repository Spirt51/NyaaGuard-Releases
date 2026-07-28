<p align="center"><img src="../assets/nyaaguard-logo.png" width="560" alt="NyaaGuard"></p>

<p align="center">
  <a href="../README.md">Русский</a> ·
  <a href="README.uk.md">Українська</a> ·
  <a href="README.en.md"><strong>English</strong></a> ·
  <a href="README.de.md">Deutsch</a>
</p>

<p align="center">
  <a href="https://github.com/Spirt51/NyaaGuard-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/Spirt51/NyaaGuard-Releases?display_name=tag&style=for-the-badge&color=b91c1c" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/Windows-x64-2563eb?style=for-the-badge&logo=windows11&logoColor=white" alt="Windows x64">
  <img src="https://img.shields.io/badge/Linux-amd64-f59e0b?style=for-the-badge&logo=linux&logoColor=white" alt="Linux amd64">
</p>

<h1 align="center">NyaaGuard</h1>
<p align="center">Link protection for Windows and Linux.<br>URL cleanup, local threat intelligence, redirect analysis, and optional VirusTotal checks.</p>

> [!IMPORTANT]
> This public repository contains official binaries and update metadata. The NyaaGuard source code is maintained in a private repository.

## Features

- intercepts external links and opens approved destinations in your selected browser;
- removes common tracking parameters such as `utm_*`, `fbclid`, `gclid`, `dclid`, `msclkid`, and other advertising or analytics identifiers;
- checks domains and exact URLs against updatable phishing, malware, and spam databases;
- provides a separate, optional adult/NSFW filter;
- inspects redirect chains and web-server response codes;
- optionally checks unknown URLs with VirusTotal using your own API key;
- supports custom block/allow lists, proxies, system theme, four interface languages, and background tray operation.

Functional parameters identifying a page, product, message, or video are preserved so cleaned links keep working. NyaaGuard then checks the resulting URL and the complete redirect chain it discovers.

## File protection in 0.3.0

- a new antivirus-style center with quick, selective, and full scans;
- scan individual files, folders, multiple drives, or the whole computer;
- SHA-256, true format detection, static analysis, and disguised-extension detection;
- isolated YARA-X with ReversingLabs rules and a curated Signature-Base subset;
- optional hash reputation through MalwareBazaar, URLhaus, and VirusTotal with user-provided API keys;
- SQLite cache and journal, pause/resume, download-folder and removable-drive monitoring;
- encrypted quarantine with SHA-256 verification during restore;
- explicit threat actions: quarantine, skip, or add the SHA-256 to exclusions;
- confirmation is required before file actions by default;
- Windows and Linux context-menu scanning for files, folders, and drives.

Scanning remains available without API keys: local hashing, format detection, heuristics, and YARA-X continue to work. File contents are not uploaded to reputation services; only the hash is queried.

Version 0.3.0 substantially accelerates the file pipeline and cache. In a 20,000-operation A/B benchmark, missing-cache lookups were up to **40.8× faster**, repeated lookups up to **50.8× faster**, and batched journal writes up to **49.5× faster** than the previous implementation. These figures cover individual cache and journal operations; whole-scan speed depends on storage, file mix, and enabled engines.

Version 0.3.0 installs application updates silently and restores the previous background-service state automatically. VirusTotal and abuse.ch keys are stored separately from application files and survive updates.

## Download

Official packages are available from the **[latest release](https://github.com/Spirt51/NyaaGuard-Releases/releases/latest)**.

| Platform | Package | Purpose |
|---|---|---|
| Windows 10/11 x64 | `NyaaGuard-Setup-*-win-x64.exe` | Install or portable extraction; optional service and shortcuts |
| Debian / Ubuntu amd64 | `nyaaguard_*_amd64.deb` | App, Native Messaging host, and systemd user service |

**Current version 0.3.0:**

- [Download for Windows x64](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/NyaaGuard-Setup-0.3.0-win-x64.exe) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/NyaaGuard-Setup-0.3.0-win-x64.exe.sha256)
- [Download for Debian/Ubuntu amd64](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/nyaaguard_0.3.0_amd64.deb) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.3.0/nyaaguard_0.3.0_amd64.deb.sha256)

Every package includes a `.sha256` file. Builds are not yet signed with a commercial certificate, so Windows SmartScreen may display a warning; verify the published SHA-256 before running a download.

## Updates and privacy

NyaaGuard checks [`update-manifest.json`](../update-manifest.json) hourly, downloads over HTTPS, and verifies SHA-256 before installation. Core checks run locally. A URL is sent to VirusTotal only when the user has configured an API key, the address is unknown to local databases, and online checks are enabled.

> [!NOTE]
> The Firefox extension is under development and is not included in published releases yet.

## Support the project

| Network | Address |
|---|---|
| USDT — TRC20 | `TR3fkALFRTDyRaHsDU8aUmANGPRDy2gU1s` |
| ETH — ERC20 | `0x9d20248c779dcb742f7795a0c7461346c0c8934e` |
| BTC | `1BQwypiKfhNGb1ryKzdp7TBPL4wR6ckU4J` |
| PayPal | `spirt51@hotmail.com` |

Always verify the network and address before sending cryptocurrency.

- **[Changelog](CHANGELOG.en.md)**
- **[Report a problem](https://github.com/Spirt51/NyaaGuard-Releases/issues)**
- **[All releases](https://github.com/Spirt51/NyaaGuard-Releases/releases)**
