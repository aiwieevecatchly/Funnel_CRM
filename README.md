# Catchly Sales Cockpit V2.6

Dieses Paket enthält **nur das Sales Cockpit** für Cold Calling, Leadbearbeitung, Wiedervorlagen, Terminierung und Übergabe ans separate Fahrplangespräch-Cockpit.

## Dateien

- `index.html` – Sales Cockpit
- `sample-leads.csv` – Beispielimport
- `assets/catchly-logo.svg` – Catchly Wortmarke
- `assets/catchly-mark.png` – Catchly Logo Mark

## Wichtigste Funktionen

- CSV/TSV/XLSX Lead-Import
- Lead-Liste mit Suche nach Firma, Kontakt, Telefon, E-Mail, Lead-ID, Ort, Branche und Status
- Lead-Zeile öffnet direkt den Live-Call
- Live-Call mit Lead-Kontext, Gatekeeper-Skripten, Einwänden und Mailbuttons
- Callback erwartet + Wiedervorlage setzen
- Fällige Wiedervorlagen werden vor neuen Leads priorisiert
- Sales-Übersicht mit Kanban, Funnel-Quoten und Zielvorgaben
- Reporting-CSV und Lead-CSV Export
- Vollbackup JSON, Restore und lokale Leads löschen
- Übergabe-Export als JSON ans separate Fahrplangespräch-Cockpit

## GitHub Upload

ZIP entpacken und nur den Inhalt des inneren Ordners in den Repository-Root hochladen:

```text
index.html
README.md
sample-leads.csv
assets/
```

Danach `Commit changes`, 1 bis 2 Minuten warten und im Browser mit `Ctrl + F5` neu laden.

## Datenschutz

Das Cockpit speichert Leads lokal im Browser (`localStorage`). GitHub stellt nur das HTML bereit. Vor Updates immer ein Backup exportieren.
