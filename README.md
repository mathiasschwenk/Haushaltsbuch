# 📒 Mein Haushaltsbuch

Eine persönliche Haushaltsbuch-App als Progressive Web App (PWA) – optimiert für GitHub Pages.

---

## 🚀 Schnellstart: Auf GitHub Pages veröffentlichen

### Schritt 1 – Repository anlegen

1. Gehe zu [github.com](https://github.com) und melde dich an
2. Klicke oben rechts auf **„+"** → **„New repository"**
3. Vergib einen Namen, z.B. `haushaltsbuch`
4. Setze das Repository auf **Public** (GitHub Pages benötigt das bei kostenlosen Konten)
5. Klicke auf **„Create repository"**

---

### Schritt 2 – Dateien hochladen

**Option A: Direkt im Browser (einfach)**

1. Öffne dein neues Repository auf GitHub
2. Klicke auf **„uploading an existing file"** oder **„Add file" → „Upload files"**
3. Ziehe **alle Dateien und Ordner** aus diesem Paket in das Upload-Fenster:
   ```
   index.html
   manifest.json
   sw.js
   .nojekyll
   icons/
     icon-192.png
     icon-512.png
   ```
   > ⚠️ Wichtig: Den Ordner `icons/` mit den Icons nicht vergessen!
4. Scrolle runter, schreibe einen Commit-Kommentar (z.B. `Initial upload`) und klicke **„Commit changes"**

**Option B: Via Git (für Fortgeschrittene)**

```bash
git clone https://github.com/DEIN-USERNAME/haushaltsbuch.git
# Kopiere alle Dateien in den geklonten Ordner
cd haushaltsbuch
git add .
git commit -m "Initial upload"
git push
```

---

### Schritt 3 – GitHub Pages aktivieren

1. Öffne dein Repository auf GitHub
2. Klicke auf **„Settings"** (oben in der Menüleiste)
3. Scrolle links zu **„Pages"**
4. Unter **„Source"**: Wähle **„Deploy from a branch"**
5. Branch: **`main`**, Ordner: **`/ (root)`**
6. Klicke **„Save"**

Nach ca. 1–2 Minuten ist die App erreichbar unter:

```
https://DEIN-USERNAME.github.io/haushaltsbuch/
```

---

## 📱 Als App installieren (PWA)

### Android (Chrome)
1. Öffne die URL im Chrome-Browser
2. Tippe auf die drei Punkte oben rechts → **„App installieren"** oder **„Zum Startbildschirm hinzufügen"**

### iPhone / iPad (Safari)
1. Öffne die URL in Safari
2. Tippe auf das **Teilen-Symbol** (Quadrat mit Pfeil nach oben)
3. Scrolle und wähle **„Zum Home-Bildschirm"**

### Desktop (Chrome / Edge)
1. Öffne die URL
2. Klicke auf das **Installieren-Symbol** in der Adressleiste (Bildschirm mit Pfeil)
3. Bestätige mit **„Installieren"**

---

## 💾 Datenspeicherung & Datenschutz

- Alle Daten werden **ausschließlich lokal** im Browser gespeichert (`localStorage`)
- Es werden **keine Daten an Server übertragen**
- Beim Löschen des Browser-Cache gehen die Daten verloren – nutze die **Export-Funktion** (Einstellungen → Datenverwaltung) für regelmäßige Backups

---

## 🔧 Dateien im Überblick

| Datei | Beschreibung |
|-------|-------------|
| `index.html` | Die komplette App (HTML + CSS + JS, alles in einer Datei) |
| `manifest.json` | PWA-Metadaten (Name, Icons, Farben, Installationsverhalten) |
| `sw.js` | Service Worker für Offline-Funktionalität und Caching |
| `.nojekyll` | Verhindert, dass GitHub Pages den Jekyll-Prozessor ausführt |
| `icons/icon-192.png` | App-Icon (192×192px, für Android/Chrome) |
| `icons/icon-512.png` | App-Icon (512×512px, für Splash Screen) |

---

## ✨ Funktionen

| Reiter | Funktion |
|--------|---------|
| 🏠 Übersicht | Aktueller Kontostand, Schnelleingabe, letzte Buchungen |
| 📋 Buchungen | Monatliche Übersicht, Buchungen hinzufügen/bearbeiten/löschen |
| 🔄 Regelmäßig | Daueraufträge verwalten (monatlich, wöchentlich, quartalsweise …) |
| 📊 Auswertung | Kuchendiagramm nach Kategorien, Säulendiagramm (6 Monate) |
| 🔮 Ausblick | Kontostandprognose bis 25 Jahre, kategorienbasierte Rhythmus-Logik |
| ⚙️ Einstellungen | Kategorien anlegen/bearbeiten/löschen, Rhythmen anpassen, Daten-Export/Import |

---

## 🔄 Updates einspielen

Wenn du eine neue Version der `index.html` erhältst:
1. Öffne dein GitHub-Repository
2. Klicke auf `index.html`
3. Klicke auf den **Stift** (Edit) oben rechts
4. Ersetze den gesamten Inhalt, oder nutze **„Upload files"** um die Datei zu überschreiben
5. Commit → die Seite wird automatisch neu gebaut

---

## ❓ Häufige Fragen

**Die App ist nach dem Upload nicht erreichbar.**
→ Warte 2–3 Minuten, GitHub Pages braucht etwas Zeit. Prüfe unter *Settings → Pages*, ob der Build erfolgreich war (grünes Häkchen).

**Die Icons werden nicht angezeigt.**
→ Stelle sicher, dass der Ordner `icons/` mit beiden PNG-Dateien hochgeladen wurde.

**Beim Öffnen als Datei (file://) funktioniert der Service Worker nicht.**
→ Das ist normal – Service Worker benötigen HTTPS oder localhost. Die App selbst funktioniert trotzdem vollständig, nur das Offline-Caching ist deaktiviert. Für volle PWA-Funktionalität bitte über GitHub Pages aufrufen.

**Ich möchte einen eigenen Domain-Namen verwenden.**
→ Erstelle eine Datei `CNAME` im Repository mit deiner Domain (z.B. `haushaltsbuch.meinedomain.de`) und konfiguriere den DNS deines Providers entsprechend.
