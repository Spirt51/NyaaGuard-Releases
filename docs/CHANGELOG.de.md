# Änderungsprotokoll

[Русский](../CHANGELOG.md) · [Українська](CHANGELOG.uk.md) · [English](CHANGELOG.en.md) · [Deutsch](CHANGELOG.de.md)

## 0.2.2 — 27. Juli 2026

- ein Hängen der normalen Installation bei der Kontextmenü-Registrierung für alle Dateien wurde behoben;
- wildcard-abhängige PowerShell-Registrierungsbefehle wurden durch die direkte Registry-API ersetzt;
- Installationsabschluss, Start der Hintergrundaufgabe und Erhalt der API-Schlüssel wurden geprüft.

## 0.2.1 — 27. Juli 2026

- NyaaGuard-Aktualisierungen laufen nach dem Beenden der App und der Hintergrundkomponente im stillen Modus;
- ein vorhandener Hintergrunddienst wird nach dem Update über die Aufgabenplanung wiederhergestellt und gestartet;
- API-Schlüssel liegen in einem dauerhaften geschützten Speicher und bleiben bei Updates erhalten;
- MalwareBazaar und URLhaus verwenden jetzt ein gemeinsames abuse.ch-Schlüsselfeld;
- eine gemeinsame Schaltfläche aktualisiert URL-Feeds, YARA-X, ReversingLabs und ausgewählte Signature-Base-Regeln;
- YARA-Regelstatus, Scan-Abbruch und automatische Kontextmenü-Registrierung wurden ergänzt.

## 0.2.0 — 27. Juli 2026

- Antivirus-Dateischutzzentrum mit Schnell-, Auswahl-, Voll- und Mehrlaufwerkprüfung hinzugefügt;
- SHA-256, Formaterkennung, statische Analyse, YARA-X, ReversingLabs und ausgewählte Signature-Base-Regeln implementiert;
- MalwareBazaar, URLhaus und VirusTotal-Dateireputation ohne Upload von Dateiinhalten hinzugefügt;
- SQLite-Cache und Journal, Pause/Fortsetzen sowie Download-/Wechseldatenträgerüberwachung ergänzt;
- verschlüsselte Quarantäne, SHA-256-geprüfte Wiederherstellung und verwaltbare Hash-Ausnahmen implementiert;
- Bedrohungsaktionen erfordern standardmäßig eine Auswahl: Quarantäne, überspringen oder ausschließen;
- System-Kontextmenüprüfung und sichere Updates mit Stopp von App und Dienst hinzugefügt;
- Dateioberfläche als professionelles Schutzzentrum in vier Sprachen neu gestaltet.

## 0.1.5 — 26. Juli 2026

- beschädigte russische und ukrainische Texte im Installer korrigiert;
- Eingabezeichenkodierung des NSIS-Skripts auf UTF-8 festgelegt;
- kompiliertes Installer-Fenster mit Windows UI Automation geprüft.

## 0.1.4 — 26. Juli 2026

- Installer-Option ergänzt, um NyaaGuard als Standard-App für HTTP/HTTPS auszuwählen;
- nach der Registrierung wird die passende Windows-Seite für Standard-Apps geöffnet;
- Schaltfläche „Als Standard festlegen“ zu den Einstellungen hinzugefügt;
- Funktion in alle vier Oberflächensprachen übersetzt.

## 0.1.3 — 26. Juli 2026

- Sprachauswahl für Russisch, Ukrainisch, Englisch und Deutsch ergänzt;
- benutzerdefinierte Seiten, Fehler und Deinstallation lokalisiert;
- gewählte Sprache für spätere Aktualisierungen gespeichert;
- Marken-Icon und großes Logo zum Installer hinzugefügt;
- Dokumentation zur Entfernung von Tracking-Parametern erweitert.

## 0.1.2 — 26. Juli 2026

- Abstände zwischen Einträgen in benutzerdefinierten Domainlisten verkleinert;
- offiziellen Link zum Abrufen eines API-Schlüssels auf der VirusTotal-Seite ergänzt;
- Oberfläche und Übersetzungen für Russisch, Ukrainisch, Englisch und Deutsch aktualisiert;
- Windows-Installer, portable Version und Debian-Paket synchronisiert.

## 0.1.1 — 26. Juli 2026

- Spendenadressen auswählbar und über das Kontextmenü kopierbar gemacht;
- nicht funktionierende Kopierschaltflächen entfernt;
- Aktualisierungsprüfung auf die GitHub Contents API umgestellt.

## 0.1.0 — 26. Juli 2026

- erste öffentliche Version für Windows x64 und Debian/Ubuntu amd64;
- URL-Bereinigung, lokale Bedrohungsdatenbanken, eigene Listen und Weiterleitungsanalyse;
- optionale VirusTotal-Prüfung, Infobereich, Proxy-Unterstützung und vier Sprachen.
