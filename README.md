# Management

Persönliche Handy-App (PWA, wie wordtime): eine index.html, keine Build-Schritte.
Erstes Modul: Habit-Tracker. UI auf Englisch (seit 20.10.2026). Weitere Module kommen als eigene Ansicht + Tab in der Unten-Navigation dazu.

## Starten
    cd ~/dev/management && python -m http.server 8081
    → http://localhost:8081

## Bedienung
- ＋ oben: Habit anlegen (Name, Symbol, Tageszeit Morgens/Tagsüber/Abends, Wochentage)
- Antippen = erledigt, lange drücken = bearbeiten
- Tagesleiste: vergangene Tage antippen und nachtragen
- Verlauf: 30-Tage-Raster, Quote und Serie je Habit
- Einstellungen: Backup speichern/laden (JSON), Habits pausieren/löschen

## Daten
localStorage (Schlüssel `management-v1`), nur auf dem Gerät. Übersteht Neustarts und Updates.
Weg nur bei: Browserdaten/Websitedaten löschen, App deinstallieren, iOS-Safari ohne Homescreen-Installation nach 7 Tagen Nichtnutzung.
Darum: `navigator.storage.persist()` wird angefragt + Backup-Funktion in den Einstellungen.

## Offen / Ideen
Live: https://businessherbst-ctrl.github.io/management/ (Updates = push auf main)

## Weitere Ideen
- Erinnerungen, weitere Module (Ziele, Finanzen, Journal …), Sync zwischen Geräten
