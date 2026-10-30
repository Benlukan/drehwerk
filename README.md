# DREHWERK

Sudoku trifft Zauberwürfel – ein Rätselspiel von david.digital.
Jede Reihe, jede Spalte und jeder Block muss jede Zahl genau einmal enthalten. Du schreibst aber keine Zahlen ein, sondern **drehst ganze Reihen und Spalten ringförmig** – wie die Scheiben eines Zauberwürfels.

**Web-Version:** https://benlukan.github.io/drehwerk/

## Modi
- **Tagesrätsel** – jeden Tag dasselbe Rätsel für alle (6×6, sonntags 9×9), Ergebnis als Emoji-Zeile teilen
- **Stufen** – Stufe 1–5: 4×4, Stufe 6–14: 6×6, ab 15: 9×9; Par steigt mit
- **Freies Spiel** – 4×4, 6×6 oder 9×9, jedes Mal neu gemischt

**Par** = Anzahl Drehungen, mit denen das Rätsel gemischt wurde. ★★★ in Par ohne Tipp, ★★ bis doppeltes Par, sonst ★.
**Tipp** zeigt immer die nächste Drehung vom aktuellen Stand aus – auf dem kürzesten bekannten Weg zur Lösung.

Steuerung: Ziehen mit Finger/Maus · am PC Feld anklicken + Pfeiltasten (Umschalt+Pfeil = Auswahl bewegen), Z = zurück, R = Neustart, H = Tipp.

## Projektstruktur
| Pfad | Inhalt |
|---|---|
| `www/` | Das komplette Spiel (eine HTML-Datei) + PWA-Manifest und Service Worker |
| `android/`, `ios/` | Native Capacitor-Projekte |
| `assets/` | Quellbilder für App-Icon und Splash (`npm run icons`) |
| `.github/workflows/` | Automatische Builds: APK, iOS-IPA, GitHub Pages |

## Builds
Jeder Push auf `main` baut automatisch – Ergebnisse unter **Actions → letzter Lauf → Artifacts**.
Ein Tag `v*` (z. B. `v1.0.0`) erstellt zusätzlich ein GitHub-Release mit den Dateien.

- `DREHWERK.apk` – direkt auf Android installierbar (Installation aus unbekannten Quellen erlauben)
- `DREHWERK-unsigned.ipa` – unsigniert; per Sideloadly/AltStore mit eigener Apple-ID installierbar
- `DREHWERK-playstore.aab` – nur wenn Release-Secrets gesetzt sind

### Play-Store-Signatur (optional)
Repository-Secrets anlegen: `ANDROID_KEYSTORE_BASE64`, `ANDROID_KEYSTORE_PASSWORD`, `ANDROID_KEY_ALIAS`, `ANDROID_KEY_PASSWORD`.

### Lokal entwickeln
```bash
npm install
npx cap sync
npx cap open android   # Android Studio
npx cap open ios       # Xcode (macOS)
```

## Version
Aktuell **v1.0.1 · Build 2** – siehe [CHANGELOG.md](CHANGELOG.md). Bei jeder Auslieferung Version + Build hochzählen in: `www/index.html` (Footer), `package.json`, `android/app/build.gradle`, `ios/App/App.xcodeproj/project.pbxproj`, `www/sw.js` (Cache-Name).
