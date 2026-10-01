# Lumen Launcher – Downloads

Willkommen im Download-Repository des **Lumen Launchers**. Hier findest du die veröffentlichten Windows-Installer und die Update-Datei, die der Launcher für seine Versionsprüfung verwendet.

## Lumen Launcher herunterladen

Öffne **[Releases](https://github.com/lennard11066-dotcom/lumen-downloads/releases/latest)** und lade dort unter **Assets** die Datei **Lumen-Setup.exe** herunter. Starte anschließend den Installer und folge den angezeigten Schritten.

> Lade Installer nur aus den Releases dieses Repositorys herunter.

## Automatische Updates

Der Launcher prüft die aktuelle Version über:

`https://github.com/lennard11066-dotcom/lumen-downloads/releases/latest/download/latest.json`

Wenn ein Update verfügbar ist, kann es im Launcher heruntergeladen und installiert werden. Schlägt die Prüfung oder der Download fehl, kannst du den aktuellen Installer jederzeit manuell über **Releases** laden.

## Releases veröffentlichen

Jeder Launcher-Release sollte diese Assets enthalten:

- `Lumen-Setup.exe` – der Installer für die neue Version
- `latest.json` – Versionsnummer, Installer-Adresse und SHA-256-Prüfsumme

Beispiel für `latest.json`:

```json
{
  "version": "1.2.0",
  "installer": "https://github.com/lennard11066-dotcom/lumen-downloads/releases/download/v1.2.0/Lumen-Setup.exe",
  "sha256": "HIER_DEN_SHA256_HASH_DES_FINALEN_INSTALLERS_EINTRAGEN",
  "notes": "Lumen Launcher 1.2.0"
}
```

Wichtig:

- Der Tag im Installer-Link muss exakt zum Release-Tag passen, zum Beispiel `v1.2.0`.
- Der SHA-256-Wert muss zum endgültigen Installer gehören. Falls der Installer signiert wird, erst signieren und danach den Hash neu berechnen.
- Ersetze im veröffentlichten `latest.json` immer den Beispieltext durch den tatsächlichen 64-stelligen Hash.
- Veröffentliche den Release erst, wenn beide Assets hochgeladen wurden.

## Hilfe bei Problemen

Wenn der Launcher nicht startet oder ein Update fehlschlägt, notiere die genaue Fehlermeldung und die installierte Launcher-Version. Bei Startproblemen mit Minecraft sind außerdem die ausgewählte Minecraft-Version und die angeforderte Java-Version hilfreich.

## Projekthinweis

Dieses Repository dient der Verteilung veröffentlichter Installer und Update-Manifeste. Änderungen am Launcher-Quellcode und Fragen zu Funktionen gehören in das jeweilige Quellcode-Repository.
