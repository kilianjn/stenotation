# Stenotation

Stenodiktat – ein Diktat-Trainer, der beliebigen Text im gewählten Tempo
(Silben pro Minute) vorliest, damit man stenografisch mitschreiben kann.

Die gesamte App steckt in einer einzelnen Datei: [`index.html`](index.html).
Sie läuft komplett im Browser, ohne Server und ohne Build-Schritt.

Mit **Als Audio speichern** lässt sich das fertige Diktat als WAV-Datei
herunterladen – mit Vorzähler, Tempo und Satzzeichenpausen genau so, wie es
auch aus dem Lautsprecher käme. Das setzt die Stimmenquelle **Piper** voraus;
die Systemstimmen des Browsers geben ihr Audio nicht heraus.

## Ausführen

**Online:** über GitHub Pages (siehe unten).

**Lokal:** `index.html` im Browser öffnen – oder, falls die Piper-Stimmen
(ES-Module vom CDN) nicht laden, einen kleinen Webserver starten:

```sh
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

## GitHub Pages einrichten

Einmalig unter **Settings → Pages** die Quelle wählen (das geht nur mit
Admin-Rechten am Repository, der Workflow kann Pages nicht selbst aktivieren):

- **Source: GitHub Actions** – danach veröffentlicht der Workflow in
  `.github/workflows/pages.yml` bei jedem Push auf `main`, oder
- **Source: Deploy from a branch** – Branch wählen, Ordner `/ (root)`.

Danach ist die Seite unter `https://kilianjn.github.io/stenotation/` erreichbar.

`.nojekyll` sorgt dafür, dass die Dateien unverändert ausgeliefert werden.
