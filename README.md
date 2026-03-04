# PIM Onboarding Checklist

Eine interaktive, minimalistische Onboarding-Checkliste für neue Teammitglieder im PIM-/E-Commerce-Umfeld.

> Ziel: Neue Kolleg:innen strukturiert durch die ersten Wochen führen – mit Fokus auf PIM-Team, Systemverständnis und allgemeinen Abläufen.

---

## Features

- Interaktive Checkboxen mit Fortschrittsanzeige
- Persistenz via `localStorage` – Fortschritt bleibt beim Schließen erhalten
- Fortschrittsbalken + Prozentanzeige pro Phase
- Strukturierte Phasen (Zugänge, Architektur, Prozesse, Stakeholder, Deliverables)
- Completion-State mit visuellem Feedback
- Reset-Funktion zum Neustart
- PDF-Export mit Fortschrittsanzeige und Status je Aufgabe
- Excel-Export mit Aufgaben-Sheet + Zusammenfassungs-Sheet
- CSV-Export (UTF-8, kompatibel mit Excel)
- Keine Dependencies – läuft komplett ohne Build-Step

---

## Nutzung

### Online öffnen

```
https://eliscodes.github.io/pm-onboarding/
```

### Lokal öffnen

```bash
git clone <repo-url>
cd pm-onboarding
open pim-onboarding-checklist.html
```

Kein Server, kein Build nötig – einfach die Datei im Browser öffnen.

### Weitergeben

Die `pim-onboarding-checklist.html` ist vollständig self-contained und kann direkt weitergegeben werden:

- Per **Teams oder Mail** als Dateianhang
- Als **Confluence-Anhang** auf der Onboarding-Seite
- Über **SharePoint / OneDrive**

Jede Person speichert ihren Fortschritt lokal im eigenen Browser – unabhängig von anderen.

### Fortschritt zurücksetzen

Über den **↺ Zurücksetzen**-Button in der App, oder manuell:

```js
localStorage.removeItem('pim-checklist');
location.reload();
```

---

## Projektstruktur

```
pm-onboarding/
├── pim-onboarding-checklist.html   # Gesamte App (HTML + CSS + JS in einer Datei)
├── index.html                      # Redirect für GitHub Pages
└── README.md
```

---

## Export-Funktionen

Alle Exporte laufen clientseitig über CDN-Libraries – kein Backend, kein Build.

| Format | Library | Inhalt |
|---|---|---|
| PDF | jsPDF 2.5.1 | Alle Phasen, Status je Aufgabe, Fortschrittsbalken |
| Excel (.xlsx) | SheetJS 0.18.5 | Sheet "Onboarding" + Sheet "Zusammenfassung" |
| CSV | nativ | Alle Aufgaben mit Phase, Typ und Status |

---

## Lizenz

© 2026 – Alle Rechte vorbehalten. Dieses Tool ist ausschließlich für den internen und privaten Gebrauch bestimmt. Weitergabe, Veröffentlichung oder Nutzung ist ohne ausdrückliche Genehmigung nicht gestattet.
