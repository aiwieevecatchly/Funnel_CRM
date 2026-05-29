# Catchly Funnel CRM v5.1

Sales-Arbeitscockpit für Kaltakquise mit fokussiertem **Script-Popup-Modus** für Live-Calls. Läuft direkt im Browser, ohne Backend, ohne Login. Speziell entwickelt für KMU aus Bau, Solar, Heizung, Sanitär, Elektro und Gebäudetechnik.

**Das CRM startet komplett leer.** Lege deine Leads manuell an, per CSV-Import oder per Excel-Import.

## Was in v5.1 neu ist

- **Script öffnet automatisch beim Call-Start** – Klick auf `📞 Call` startet den Lead **und** öffnet sofort das Script-Modal
- **Live-Call-Reiter radikal aufgeräumt** – keine doppelten Buttonleisten, kein duplizierter Script-Bereich. Nur: kompakte Lead-Daten, Quick-Actions, Schnellabschluss, Call-Log
- **Direkt-Shortcuts im Script-Modal** – sechs Action-Buttons in einer Leiste: Fahrplangespräch buchen, Ready Check starten, Termin bestätigen, Infomail vorbereiten, Speichern · nächster Lead, Kein Interesse
- **Logo aus Brand-Sheet** – SVG-Rekonstruktion exakt nach den Brand Guidelines (gelbes Quadrat, pinkes Dreieck/Diamant/Kreis, indigo Ellipse, Modak-Schriftzug)
- **Modak via Google Fonts** – der originale Catchly-Schriftzug wird beim Öffnen geladen
- **Neon Pink korrigiert auf `#FE0B7D`** (zuvor `#FE007D`) – exakt nach Brand-Sheet
- **CRM startet leer** – keine Demo-Leads im Auslieferungszustand. Du arbeitest sofort mit deinen echten Daten

## Logo einbauen

Lege deine Logo-Datei genau hier ab:

```
assets/catchly-logo.png
```

Empfohlene Höhe: 180–300 px, transparenter Hintergrund, PNG-Format. Sobald die Datei am richtigen Ort liegt, wird sie automatisch im Header angezeigt statt der SVG-Annäherung.

## Wichtig zum Thema Leads-Speicherung

Alle Daten werden im **Browser-localStorage** gespeichert. Das ist eine Browser-Funktion, kein Cloud-Speicher. Daher:

- Daten bleiben **pro Browser, pro Gerät und pro Pfad/Origin** erhalten
- Wenn du die Datei aus einem anderen Ordner öffnest, sieht der Browser das als andere App
- **Lösung**: Immer aus dem selben Ordner arbeiten – oder auf GitHub Pages hosten (URL bleibt stabil)
- **Beim Wechsel auf eine neue Version**: vorher in der alten Version *Excel Export* klicken, in der neuen Version importieren
- Beim Löschen des Browser-Cache gehen die Daten verloren – regelmässig Export klicken

## So nutzt du den Cold Call (v5.1 Workflow)

1. Lead in der Lead-Tabelle wählen → `📞 Call` klicken
2. **Sofort öffnet sich das Script-Modal mit dem Gatekeeper-Einstieg** – du siehst Wortlaut, Hinweis, Karten direkt
3. Pfeil rechts ‹ › → nächster Schritt. Tab oben → anderer Flow (Gatekeeper / Entscheider / Einwände / Follow-up / Abschluss)
4. Wenn der Kunde einen Einwand bringt: Chip unten klicken → passender Einwand-Block erscheint im selben Modal mit Kurzantwort, Gegenfrage und Nächster Schritt
5. **Direkt-Shortcuts in der Action-Leiste**:
   - **Fahrplangespräch buchen** → öffnet 4-Step-Fahrplan-Wizard
   - **Ready Check starten** → öffnet 8-Fragen-Modal
   - **Termin bestätigen** → setzt Status, öffnet Mail-Vorlage
   - **Infomail vorbereiten** → setzt Status, springt in Mail-Tab
   - **Speichern · nächster Lead** → springt zum nächsten Lead in der Queue, öffnet wieder das Script-Modal
   - **Kein Interesse** → markiert, springt weiter
6. Im Hintergrund läuft die Schnellabschluss-Leiste im Live-Call-Reiter für Notizen und Follow-up-Datum

## Script-Editor

Im Tab **Call Scripts** kannst du alle Flows direkt bearbeiten – Text, Reihenfolge, aktivieren/deaktivieren, neue Schritte, neue Karten. Variablen `{{firma}}`, `{{kontaktperson}}`, `{{funktion}}`, `{{branche}}`, `{{region}}` werden im Live-Call automatisch ersetzt.

## Excel-Export

Im Tab **Leads** den Button *Excel Export* klicken. Beim ersten Klick lädt SheetJS einmalig aus dem CDN (Internet beim ersten Mal nötig). Datei `catchly_crm_export_YYYY-MM-DD.xlsx` mit vier Tabs (Leads / Call Logs / Pipeline / Tagesleistung).

## Installation

### 1. Lokal öffnen

Diesen Ordner herunterladen, entpacken und `index.html` per Doppelklick öffnen.

### 2. Über GitHub Pages hosten (empfohlen für stabile URL)

1. Neues Repository auf GitHub erstellen
2. Den kompletten Ordnerinhalt hochladen
3. **Settings → Pages → Source: main / (root)**
4. Nach 1–2 Minuten erreichbar unter `https://DEINNAME.github.io/REPO-NAME/`

## Brand und Schrift

- Indigo `#541388`
- Gold `#FFD400`
- Neon Pink `#FE0B7D`
- Weiss `#FFFFFF`, Schwarz `#000000`
- Primary Font: **Modak** (Headlines, Logo) – über Google Fonts geladen
- Secondary/Body Font: **Nunito**

## Funnel-Stufen

15 Stufen: Importiert → Anwahlversuch → Zielperson erreicht → Rückruf → Infomail → Fahrplangespräch gebucht → Fahrplangespräch durchgeführt → Ready Check offen → Ready Check abgeschlossen → Sales Assessment angeboten/gebucht/durchgeführt → Angebot offen → Abschluss gewonnen/verloren

## Ordnerstruktur

```
Catchly_funnel_crm/
├── index.html              ← die App
├── README.md               ← diese Datei
├── assets/
│   ├── catchly-logo.png    ← dein Logo (hier ablegen)
│   └── README.txt          ← Logo-Hinweis
└── data/
    ├── demo-leads.json     ← leer (CRM startet ohne Demo-Daten)
    └── leads-template.csv  ← Import-Vorlage
```

## Lizenz

Internes Tool von Catchly. Eve Wietlisbach.
