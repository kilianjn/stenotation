# Stenotation

Stenodiktat – ein Diktat-Trainer, der beliebigen Text im gewählten Tempo
(Silben pro Minute) vorliest, damit man stenografisch mitschreiben kann.

Die gesamte App steckt in einer einzelnen Datei: [`index.html`](index.html).
Sie läuft komplett im Browser, ohne Server und ohne Build-Schritt.

## Ausführen

**Online:** über GitHub Pages (siehe unten).

**Lokal:** `index.html` im Browser öffnen – oder, falls die Piper-Stimmen
(ES-Module vom CDN) nicht laden, einen kleinen Webserver starten:

```sh
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

## GitHub Pages einrichten

Einmalig unter **Settings → Pages**:

- **Source: GitHub Actions** – der Workflow in
  `.github/workflows/pages.yml` veröffentlicht dann bei jedem Push, oder
- **Source: Deploy from a branch** – Branch wählen, Ordner `/ (root)`.

Danach ist die Seite unter `https://kilianjn.github.io/stenotation/` erreichbar.

`.nojekyll` sorgt dafür, dass die Dateien unverändert ausgeliefert werden.
