# Osteopathie Darmstadt – Onepager

Statische Website ohne JavaScript, Cookies oder Tracking. Alles Veröffentlichte liegt in `public/`.

## Ordner
- `public/` – Seiten (index, impressum, datenschutz, agb, 404), `assets/` mit CSS und Bildern
- `netlify.toml` – Veröffentlichungsordner, Sicherheits-Header

## 1. Vor dem Hochladen erledigen
1. `public/impressum.html`: Gelb markiertes Feld „Zuständiges Gesundheitsamt eintragen“ ersetzen (mark-Tag entfernen).
2. Impressum/Datenschutz/AGB von einer fachkundigen Stelle prüfen lassen.
3. Sobald die Domain feststeht: `<link rel="canonical">` und eine `sitemap.xml` ergänzen.

## 2. GitHub
1. Auf github.com ein neues, leeres Repository anlegen (z. B. `osteopathie-darmstadt`).
2. „uploading an existing file“ wählen und den **Inhalt dieses Ordners** hineinziehen (`public/`, `netlify.toml`, `README.md`), dann „Commit changes“.

## 3. Netlify
1. Auf netlify.com mit GitHub anmelden → „Add new project“ → „Import an existing project“ → GitHub → Repository wählen.
2. Build command leer lassen, Publish directory `public` (steht bereits in `netlify.toml`). „Deploy“.
3. Die Seite ist danach unter `xyz.netlify.app` erreichbar. Jede Änderung im Repository veröffentlicht automatisch neu.

## 4. Domain bei INWX
1. Domain bei INWX registrieren.
2. In Netlify: Domain management → „Add a domain“ → Domain eintragen.
3. Bei INWX unter Nameserver/DNS die von Netlify genannten Einträge setzen (meist `A`-Record für die Hauptdomain auf die genannte Netlify-IP und `CNAME` für `www` auf `<projektname>.netlify.app`; es gelten die aktuellen Werte, die Netlify anzeigt).
4. In Netlify „Verify DNS“ und danach unter HTTPS das kostenlose Zertifikat aktivieren („Let's Encrypt“). „Force HTTPS“ einschalten.

## 5. Prüfliste nach dem Start
- Telefon- und Mail-Links testen (Handy)
- Impressum, Datenschutz, AGB erreichbar
- Aufsichtsbehörde eingetragen
- Zeiten ergänzen, falls gewünscht (derzeit „dienstags, nach Vereinbarung“)
