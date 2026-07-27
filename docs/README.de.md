<p align="center"><img src="../assets/nyaaguard-logo.png" width="560" alt="NyaaGuard"></p>

<p align="center">
  <a href="../README.md">Русский</a> ·
  <a href="README.uk.md">Українська</a> ·
  <a href="README.en.md">English</a> ·
  <a href="README.de.md"><strong>Deutsch</strong></a>
</p>

<p align="center">
  <a href="https://github.com/Spirt51/NyaaGuard-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/Spirt51/NyaaGuard-Releases?display_name=tag&style=for-the-badge&color=b91c1c" alt="Neueste Version"></a>
  <img src="https://img.shields.io/badge/Windows-x64-2563eb?style=for-the-badge&logo=windows11&logoColor=white" alt="Windows x64">
  <img src="https://img.shields.io/badge/Linux-amd64-f59e0b?style=for-the-badge&logo=linux&logoColor=white" alt="Linux amd64">
</p>

<h1 align="center">NyaaGuard</h1>
<p align="center">Linkschutz für Windows und Linux.<br>URL-Bereinigung, lokale Bedrohungsdaten, Weiterleitungsanalyse und optionale VirusTotal-Prüfung.</p>

> [!IMPORTANT]
> Dieses öffentliche Repository enthält offizielle Binärdateien und Aktualisierungsmetadaten. Der NyaaGuard-Quellcode wird in einem privaten Repository gepflegt.

## Funktionen

- fängt externe Links ab und öffnet freigegebene Ziele im ausgewählten Browser;
- entfernt verbreitete Tracking-Parameter wie `utm_*`, `fbclid`, `gclid`, `dclid`, `msclkid` und weitere Werbe- oder Analysekennungen;
- prüft Domains und exakte URLs anhand aktualisierbarer Phishing-, Malware- und Spam-Datenbanken;
- bietet einen separaten, abschaltbaren Adult-/NSFW-Filter;
- untersucht Weiterleitungsketten und HTTP-Antwortcodes;
- prüft unbekannte URLs optional über VirusTotal mit dem eigenen API-Schlüssel;
- unterstützt eigene Sperr- und Ausnahmelisten, Proxy, Systemdesign, vier Sprachen und den Betrieb im Infobereich.

Funktionale Parameter für Seite, Produkt, Nachricht oder Video bleiben erhalten, damit bereinigte Links funktionieren. Anschließend prüft NyaaGuard die resultierende URL und die vollständig erkannte Weiterleitungskette.

## Dateischutz in 0.2.0

- neues Antivirus-Zentrum mit Schnell-, Auswahl- und Vollprüfung;
- einzelne Dateien, Ordner, mehrere Laufwerke oder den gesamten Computer prüfen;
- SHA-256, echte Formaterkennung, statische Analyse und Erkennung getarnter Erweiterungen;
- isoliertes YARA-X mit ReversingLabs-Regeln und ausgewählten Signature-Base-Regeln;
- optionale Hash-Reputation über MalwareBazaar, URLhaus und VirusTotal mit eigenen API-Schlüsseln;
- SQLite-Cache und Journal, Pause/Fortsetzen sowie Überwachung von Downloads und Wechseldatenträgern;
- verschlüsselte Quarantäne mit SHA-256-Prüfung beim Wiederherstellen;
- eindeutige Bedrohungsaktionen: Quarantäne, überspringen oder SHA-256 ausschließen;
- Dateiaktionen erfordern standardmäßig eine Bestätigung;
- Kontextmenüprüfung für Dateien, Ordner und Laufwerke unter Windows und Linux.

Die Prüfung funktioniert ohne API-Schlüssel weiter: lokales Hashing, Formaterkennung, Heuristik und YARA-X bleiben verfügbar. Dateiinhalte werden nicht an Reputationsdienste hochgeladen; abgefragt wird nur der Hash.

## Download

Offizielle Pakete stehen im **[neuesten Release](https://github.com/Spirt51/NyaaGuard-Releases/releases/latest)** bereit.

| System | Paket | Verwendung |
|---|---|---|
| Windows 10/11 x64 | `NyaaGuard-Setup-*-win-x64.exe` | Installation oder portables Entpacken; Dienst und Verknüpfungen optional |
| Debian / Ubuntu amd64 | `nyaaguard_*_amd64.deb` | Anwendung, Native-Messaging-Host und systemd-Benutzerdienst |

**Aktuelle Version 0.2.0:**

- [Für Windows x64 herunterladen](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/NyaaGuard-Setup-0.2.0-win-x64.exe) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/NyaaGuard-Setup-0.2.0-win-x64.exe.sha256)
- [Für Debian/Ubuntu amd64 herunterladen](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/nyaaguard_0.2.0_amd64.deb) · [SHA-256](https://github.com/Spirt51/NyaaGuard-Releases/releases/download/v0.2.0/nyaaguard_0.2.0_amd64.deb.sha256)

Zu jedem Paket gehört eine `.sha256`-Datei. Die Builds sind noch nicht mit einem kommerziellen Zertifikat signiert; Windows SmartScreen kann deshalb warnen. Prüfen Sie vor dem Start den veröffentlichten SHA-256-Wert.

## Aktualisierung und Datenschutz

NyaaGuard prüft [`update-manifest.json`](../update-manifest.json) stündlich, lädt Pakete per HTTPS und verifiziert vor der Installation SHA-256. Die Kernprüfungen laufen lokal. Eine URL wird nur an VirusTotal gesendet, wenn ein API-Schlüssel eingerichtet wurde, die Adresse in den lokalen Datenbanken unbekannt ist und die Online-Prüfung aktiviert ist.

> [!NOTE]
> Die Firefox-Erweiterung befindet sich noch in Entwicklung und ist noch nicht Bestandteil der veröffentlichten Releases.

## Projekt unterstützen

| Netzwerk | Adresse |
|---|---|
| USDT — TRC20 | `TR3fkALFRTDyRaHsDU8aUmANGPRDy2gU1s` |
| ETH — ERC20 | `0x9d20248c779dcb742f7795a0c7461346c0c8934e` |
| BTC | `1BQwypiKfhNGb1ryKzdp7TBPL4wR6ckU4J` |
| PayPal | `spirt51@hotmail.com` |

Prüfen Sie vor einer Kryptowährungsüberweisung immer Netzwerk und Adresse.

- **[Änderungsprotokoll](CHANGELOG.de.md)**
- **[Problem melden](https://github.com/Spirt51/NyaaGuard-Releases/issues)**
- **[Alle Releases](https://github.com/Spirt51/NyaaGuard-Releases/releases)**
