# Changelog

## v1.2.0 (Build 4) – 30.10.2026
- Neu: **Einstellungen** (⚙ oben rechts und im Menü)
  - Ton, Vibration (Haptik in der App), Animation Normal/Schnell
  - Farben: Bunt / Farbsicher (für Farbsehschwäche) / Grau (reines Zahlen-Sudoku)
  - Zahlen auf Steinen an/aus (nur nach Farben spielen), Fortschritts-Anzeige an/aus
  - Stufen-Fortschritt löschen (mit Bestätigung), Werbe-Einstellungen, Datenschutzerklärung
- Neu: **„‹ Menü“-Knopf** oben links – pausiert das Rätsel, „Weiter“ setzt es fort
- Android: Zurück-Taste führt ins Menü bzw. schließt Einstellungen; im Menü beendet sie die App
- Einstellungen werden gespeichert; bisherige Ton-Einstellung wird übernommen

## v1.1.0 (Build 3) – 30.10.2026
- Werbung in der Android-/iOS-App über Google AdMob (vorerst Test-IDs); Web-Version und Tagesrätsel bleiben werbefrei
  - 1 Tipp pro Rätsel gratis, weitere per freiwilligem Video (ohne verfügbares Video gratis)
  - Vollbild-Werbung nach jedem 3. gelösten Rätsel, in den Stufen erst ab Stufe 5, nie mitten im Rätsel
  - Einwilligungsfenster (Google UMP) beim ersten Start, „Werbe-Einstellungen“ im Menü; iOS-Tracking-Abfrage
- Neue Datenschutzerklärung (`datenschutz.html`), Link im Menü und in der Fußzeile
- Schrift liegt jetzt lokal in der App (keine Verbindung zu Google Fonts)

## v1.0.1 (Build 2) – 30.10.2026
- Tipp geht jetzt immer vom aktuellen Stand aus: zeigt die nächste Drehung auf dem kürzesten bekannten Weg (Vorwärtssuche + Abkürzungen), kein „Züge zurücknehmen“ mehr
- Tipp nennt die Restlänge („noch höchstens X Züge“)

## v1.0.0 (Build 1) – 30.10.2026
- Erste Version: Sudoku-Regeln mit Zauberwürfel-Mechanik – Reihen und Spalten ringförmig drehen
- Spielfelder 4×4, 6×6 und 9×9 mit Blöcken (2×2, 2×3, 3×3)
- Modi: Tagesrätsel (sonntags 9×9) mit Teilen-Funktion, 30+ Stufen, Freies Spiel
- Live-Anzeige: grüne Randmarken für fertige Reihen/Spalten, grüne Rahmen für fertige Blöcke – schon während des Ziehens
- Par-Wertung mit Sternen, Zähler, Zeit, Zurück, Neustart, Tipp
- Tastatursteuerung am PC
- Installierbar als Web-App (PWA, offline spielbar), Android- und iOS-App (Capacitor), nur Hochformat
