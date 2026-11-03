# Planwerk

**English** · [Deutsch](#deutsch)

Planwerk is a project planning tool that runs entirely in your browser. It is a single HTML file with no server, no account and no installation, and it works offline.

## Tools

| Tool | What it does |
|---|---|
| **Work breakdown structure (WBS)** | Break the project down into phases, summary tasks and work packages. WBS codes (1, 1.1, 1.1.2 …) are assigned automatically. Hybrid or tree layout. |
| **Gantt chart** | Schedule with day, week and month views, dependencies, total float, critical path, milestones, progress and a today line. Weekends and public holidays are skipped. |
| **Network diagram** | Activity-on-node network with forward and backward pass (ES, EF, LS, LF, TF, FF). The critical path is highlighted. |
| **Risk matrix** | 5 × 5 matrix of probability and impact, with a risk register, strategy, mitigation, owner, status and residual risk. |
| **PDF editor** | Open any PDF and add text, pen drawings, highlights, boxes and arrows, or cover areas. Add or delete pages. Save as PDF or Word. |
| **Save as** | Export to PDF, Word (.docx), PNG, SVG, HTML report or a JSON project file. |
| **My projects** | Keep several projects side by side, duplicate them, back them up as files or load them again. |

All plans share the same data. A change in one view shows up in all the others.

## Features

- **Edit right in the diagram.** Double-click to rename, drag to move, drag a bar edge to change a duration, drag a handle to link tasks, right-click for all actions.
- **Readable PDF export.** A minimum font size is kept. Large plans are split across several pages, and the cuts fall between elements, so no box is ever cut in half. An overview page shows how the pages fit together.
- **Dependency types** FS, SS, FF and SF, with lag in days.
- **Start constraints**, colours, notes and collapsible groups.
- **Templates**: empty project, ticket system example, IT apprenticeship final project, website, event.
- **Light and dark mode**, accent colour and font size settings.
- **English and German.**
- **Keyboard shortcuts**: Enter, Tab, Del, F2, Ctrl+Z/Y, Ctrl+C/V, Ctrl+D, Ctrl+F, Ctrl+S. Press `?` in the app for the full list.
- **Dockable panels.** Collapse the sidebar or drag it and the task table to the other side.
- **Works on phones and tablets.**

## Getting started

Open `index.html` in Chrome, Edge or Firefox. That's it.

To host it on **GitHub Pages**: put `index.html` in a public repository, then go to *Settings → Pages* and choose *Deploy from a branch → main → / (root)*.

## Where is my data?

Everything is saved automatically in your own browser, in both localStorage and IndexedDB. Nothing is uploaded anywhere.

- Every browser and device has its own data. Use *My projects → Back up all as a file* to move projects to another device.
- Private windows and clearing browser data delete your projects. Back up important projects as a file.

## Built with

These libraries are embedded in the file, so it works without an internet connection:

- [pdf-lib](https://github.com/Hopding/pdf-lib) 1.17.1 · MIT
- [PDF.js](https://github.com/mozilla/pdf.js) 3.11.174 · Apache 2.0
- [JSZip](https://github.com/Stuk/jszip) 3.10.1 · MIT

---

<a id="deutsch"></a>

# Planwerk

[English](#planwerk) · **Deutsch**

Planwerk ist ein Projektplanungs-Tool, das komplett im Browser läuft. Es besteht aus einer einzigen HTML-Datei, braucht keinen Server, kein Konto und keine Installation, und es funktioniert auch offline.

## Tools

| Tool | Was es macht |
|---|---|
| **Projektstrukturplan (PSP)** | Projekt in Phasen, Teilaufgaben und Arbeitspakete gliedern. Die PSP-Codes (1, 1.1, 1.1.2 …) werden automatisch vergeben. Darstellung als Mischform oder Baum. |
| **Gantt-Diagramm** | Zeitplan mit Tages-, Wochen- und Monatsansicht, Abhängigkeiten, Gesamtpuffer, kritischem Pfad, Meilensteinen, Fortschritt und Heute-Linie. Wochenenden und Feiertage werden übersprungen. |
| **Netzplan** | Vorgangsknotennetzplan mit Vorwärts- und Rückwärtsrechnung (FAZ, FEZ, SAZ, SEZ, GP, FP). Der kritische Pfad wird hervorgehoben. |
| **Risikomatrix** | 5 × 5-Matrix aus Eintrittswahrscheinlichkeit und Auswirkung, mit Risikoliste, Strategie, Maßnahme, Verantwortlichen, Status und Restrisiko. |
| **PDF-Editor** | Beliebige PDFs öffnen und mit Text, Stift, Markierungen, Rahmen und Pfeilen beschriften oder Stellen abdecken. Seiten hinzufügen oder löschen. Speichern als PDF oder Word. |
| **Speichern als** | Export als PDF, Word (.docx), PNG, SVG, HTML-Bericht oder JSON-Projektdatei. |
| **Meine Projekte** | Mehrere Projekte nebeneinander verwalten, duplizieren, als Datei sichern oder wieder laden. |

Alle Pläne nutzen dieselben Daten. Eine Änderung in einer Ansicht ist sofort in allen anderen sichtbar.

## Funktionen

- **Direkt im Diagramm bearbeiten.** Doppelklick benennt um, Ziehen verschiebt, die Balkenkante ändert die Dauer, ein Griff verknüpft Vorgänge, Rechtsklick zeigt alle Aktionen.
- **Lesbarer PDF-Export.** Eine Mindestschriftgröße wird eingehalten. Große Pläne werden auf mehrere Seiten verteilt, und die Schnitte liegen zwischen den Elementen, damit keine Box halb abgeschnitten wird. Eine Übersichtsseite zeigt, wie die Seiten zusammengehören.
- **Anordnungsbeziehungen** EA, AA, EE und AE, mit Zeitabstand in Tagen.
- **Fixtermine**, Farben, Notizen und einklappbare Gruppen.
- **Vorlagen**: leeres Projekt, Beispiel Ticketsystem, IHK-Abschlussprojekt, Website, Veranstaltung.
- **Hell- und Dunkelmodus**, einstellbare Akzentfarbe und Schriftgröße.
- **Deutsch und Englisch.**
- **Tastenkürzel**: Enter, Tab, Entf, F2, Strg+Z/Y, Strg+C/V, Strg+D, Strg+F, Strg+S. In der App zeigt `?` die vollständige Liste.
- **Andockbare Leisten.** Die Seitenleiste lässt sich einklappen, und sie und die Vorgangstabelle lassen sich auf die andere Seite ziehen.
- **Läuft auch auf Handy und Tablet.**

## Loslegen

`index.html` in Chrome, Edge oder Firefox öffnen. Fertig.

Für **GitHub Pages**: `index.html` in ein öffentliches Repository legen, dann unter *Settings → Pages* die Option *Deploy from a branch → main → / (root)* wählen.

## Wo sind meine Daten?

Alles wird automatisch in deinem eigenen Browser gespeichert, in localStorage und zusätzlich in IndexedDB. Nichts wird irgendwohin hochgeladen.

- Jeder Browser und jedes Gerät hat eigene Daten. Mit *Meine Projekte → Alle als Datei sichern* nimmst du Projekte auf ein anderes Gerät mit.
- In privaten Fenstern und beim Löschen der Browserdaten gehen die Projekte verloren. Wichtige Projekte deshalb zusätzlich als Datei sichern.

## Verwendete Bibliotheken

Diese Bibliotheken sind direkt in die Datei eingebettet, deshalb funktioniert sie ohne Internet:

- [pdf-lib](https://github.com/Hopding/pdf-lib) 1.17.1 · MIT
- [PDF.js](https://github.com/mozilla/pdf.js) 3.11.174 · Apache 2.0
- [JSZip](https://github.com/Stuk/jszip) 3.10.1 · MIT
