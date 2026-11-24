# Stenotation

Stenodiktat – ein Diktat-Trainer, der beliebigen Text im gewählten Tempo
(Silben pro Minute) vorliest, damit man stenografisch mitschreiben kann.

Die gesamte App steckt in einer einzelnen Datei: [`index.html`](index.html).
Sie läuft komplett im Browser, ohne Server und ohne Build-Schritt.

Mit **Als Audio speichern** lässt sich das fertige Diktat als MP3 herunterladen
– mit Vorzähler, Tempo und Satzzeichenpausen genau so, wie es auch aus dem
Lautsprecher käme. Das setzt die Stimmenquelle **Piper** voraus (die Vorgabe);
die Systemstimmen des Browsers geben ihr Audio nicht heraus. Der MP3-Encoder
wird beim ersten Speichern vom CDN nachgeladen; ist er nicht erreichbar,
entsteht stattdessen eine WAV-Datei.

Das Häkchen **Text wiederholen** lässt das Diktat nach dem letzten Wort wieder
von vorn beginnen, bis man pausiert.

## Ausführen

**Online:** über GitHub Pages (siehe unten).

**Lokal:** `index.html` im Browser öffnen – oder, falls die Piper-Stimmen
(ES-Module vom CDN) nicht laden, einen kleinen Webserver starten:

```sh
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

## GitHub Pages einrichten

Die Seite liegt unter `https://kilianjn.github.io/stenotation/` und wird von
GitHub direkt aus dem Branch veröffentlicht: **Settings → Pages → Source:
Deploy from a branch**, Branch `main`, Ordner `/ (root)`. Jeder Push auf
`main` erneuert sie, ein eigener Workflow ist dafür nicht nötig.

`.nojekyll` sorgt dafür, dass die Dateien unverändert ausgeliefert werden.
