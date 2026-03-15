# CUT PROTOCOL — PWA

Offline-fähige Progressive Web App für Android. Kein Server nötig.

## Deployment via GitHub Pages (kostenlos, 2 Minuten)

1. GitHub-Repo erstellen (z.B. `cut-protocol`)
2. Alle Dateien aus diesem Ordner ins Repo pushen
3. Settings → Pages → Source: "Deploy from a branch" → Branch: `main` → Ordner: `/ (root)` → Save
4. Nach ~1 Minute: `https://dein-username.github.io/cut-protocol/`
5. Auf dem Handy öffnen → Chrome-Menü (⋮) → "App installieren" oder "Zum Startbildschirm hinzufügen"

## Dateien

```
index.html      ← Komplette App (HTML + CSS + JS inline)
manifest.json   ← PWA-Manifest (Name, Icon, Farben)
sw.js           ← Service Worker (Offline-Cache)
icon-192.png    ← App-Icon 192×192
icon-512.png    ← App-Icon 512×512
```

## Hinweis

Wenn das Repo NICHT `dein-username.github.io` heißt (sondern z.B. `cut-protocol`),
dann muss in `manifest.json` die `start_url` angepasst werden:

```json
"start_url": "/cut-protocol/"
```

Und in `index.html` der Service-Worker-Pfad:
```js
navigator.serviceWorker.register('/cut-protocol/sw.js')
```
