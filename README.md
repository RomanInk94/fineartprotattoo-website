# fineartprotattoo.com

Quellcode der Website von Roman Olichowski (FineArt Pro Tattoo).
Statische Seite, kein Build-Schritt, kein Framework.

## Aufbau

| Pfad | Inhalt |
|---|---|
| `index.html` | Startseite (CSS und JS inline) |
| `events/index.html` | Event-Tattoos |
| `blog/tattoo-nachsorge.html` | Blogbeitrag |
| `impressum.html` | Impressum (§ 5 DDG) |
| `datenschutz.html` | Datenschutzerklärung (DSGVO) |
| `images/`, `events/images/` | Bilder |
| `_redirects` | Saubere URLs: `/impressum`, `/datenschutz` |
| `_headers` | Sicherheits-Header (CSP usw.) |
| `robots.txt`, `sitemap.xml`, `llms.txt` | Suchmaschinen |

## Änderungen veröffentlichen

Netlify hängt an diesem Repository. Jeder Push auf `main` geht automatisch live:

```
git add -A
git commit -m "was geaendert wurde"
git push
```

Nach ein bis zwei Minuten ist die Änderung auf https://fineartprotattoo.com sichtbar.
Zurückrollen geht bei Netlify unter *Deploys* mit einem Klick auf einen
früheren Stand ("Publish deploy").

## Achtung

- Es gibt **keinen Build-Schritt**. Build command bleibt leer, Publish directory ist das
  Wurzelverzeichnis.
- `_headers` und `_redirects` müssen im Wurzelverzeichnis bleiben, sonst fallen
  Sicherheits-Header und die URLs ohne `.html` weg.
- Die Schriften werden noch von Google geladen (siehe offener Punkt in der
  Datenschutzerklärung, Ziffer 4).
