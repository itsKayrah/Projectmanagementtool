# ProjectKit

**English** · [Deutsch](#deutsch)

ProjectKit is a project planning tool that runs entirely in your browser. No server, no account, no tracking. It can be installed as an app and works offline.

## Tools

| Tool | What it does |
|---|---|
| **Work breakdown structure (WBS)** | Break the project down into phases, summary tasks and work packages. WBS codes (1, 1.1, 1.1.2 …) are assigned automatically. Hybrid or tree layout. |
| **Gantt chart** | Schedule with day, week and month views, dependencies, total float, critical path, milestones, progress and a today line. Weekends and public holidays are skipped. |
| **Network diagram** | Activity-on-node network with forward and backward pass (ES, EF, LS, LF, TF, FF). The critical path is highlighted. |
| **Risk matrix** | 5 × 5 matrix of probability and impact, with a risk register, strategy, mitigation, owner, status and residual risk. |
| **Costs and economics** | Personnel costs calculated from the plan (duration × hours per day × hourly rate), workplace, material and external costs, yearly benefit, static payback calculation with chart, and a weighted utility analysis to compare options. |
| **Diagrams (UML and ER)** | Use case and activity diagrams, plus ER diagrams in Chen notation (entities, relationships, attributes, cardinalities) and crow's foot notation (tables with PK/FK). A notation check flags common mistakes. |
| **PDF editor** | Open any PDF, edit its existing text lines, and add text, notes, pen and marker strokes, highlights, rectangles, ellipses, lines, arrows, images, stamps and your own signature, or cover areas. Everything stays selectable, movable, resizable and rotatable, with a properties panel for colours, fill, opacity, line style, fonts and image adjustments. Pixel and object eraser. Move, rotate, duplicate, insert or delete pages. Save as PDF or Word. |
| **Save as** | Export to PDF, Word (.docx), PNG, SVG, HTML report or a JSON project file. |
| **My projects** | Keep several projects side by side, duplicate them, back them up as files or load them again. |

All plans share the same data. A change in one view shows up in all the others.

## Features

- **Edit right in the diagram.** Double-click to rename, drag to move, drag a bar edge to change a duration, drag a handle to link tasks, right-click for all actions.
- **Diagram editor:** centre snapping and alignment guides keep lines straight, draggable anchor points change a line's course, line ends can be reconnected, and every element has its own fill, text colour, font size, bold/italic, alignment and line style. Ctrl+Shift+C/V copies a format.
- **Touch:** pan with one finger, pinch to zoom, long-press for the menu.
- **Readable PDF export.** A minimum font size is kept. Large plans are split across several pages, and the cuts fall between elements, so no box is ever cut in half.
- **Dependency types** FS, SS, FF and SF, with lag in days.
- **Templates**: empty project, ticket system example, IT apprenticeship final project, website, event.
- **Light and dark mode**, accent colour and font size settings.
- **English and German.**
- **Keyboard shortcuts.** Press `?` in the app for the full list.
- **Menu bar** (File, Edit, View, Window, Help) like in desktop programs.
- **Dockable, resizable sidebar and panels.**

## Getting started

**Online:** open the GitHub Pages link of this repository. In Chrome or Edge you can then choose *Settings → App → Install*, on iPhone *Share → Add to Home Screen*.

**Offline as a single file:** open `docs/projectkit.html` straight from your disk. It contains everything it needs.

## Host it on GitHub Pages

1. Push this repository to GitHub.
2. Go to *Settings → Pages*, choose *Deploy from a branch*, branch `main`, folder `/docs`.
3. After a minute the app is live and installable.

## Development

The source is split into small files in `src/`. The build merges them into one file and needs nothing but Node.js:

```
node build.js
```

| Path | Contents |
|---|---|
| `src/index.html` | Markup, loads the CSS and JS files in order |
| `src/css/` | Styles, one file per area |
| `src/js/` | App code, numbered in load order (core, i18n, model, views, diagrams, costs, export, storage …) |
| `src/vendor/` | Embedded libraries |
| `src/icons/` | App icons |
| `docs/` | Build output: `index.html` (PWA with service worker and manifest) and `projectkit.html` (single file) |
| `test/smoke.py` | Playwright smoke test: `python3 test/smoke.py docs/projectkit.html` |

During development you can also open `src/index.html` directly, without building.

## Where is my data?

Everything is saved automatically in your own browser, in both localStorage and IndexedDB. Settings, including which tips you've closed, are stored too. Nothing is uploaded anywhere.

- Every browser and device has its own data. Use *My projects → Back up all as a file* to move projects to another device.
- Private windows and clearing browser data delete your projects. Back up important projects as a file.

## Built with

These libraries are embedded, so the app works without an internet connection:

- [pdf-lib](https://github.com/Hopding/pdf-lib) 1.17.1 · MIT
- [PDF.js](https://github.com/mozilla/pdf.js) 3.11.174 · Apache 2.0
- [JSZip](https://github.com/Stuk/jszip) 3.10.1 · MIT

---

<a id="deutsch"></a>

# ProjectKit

[English](#projectkit) · **Deutsch**

ProjectKit ist ein Projektplanungs-Tool, das komplett im Browser läuft. Kein Server, kein Konto, kein Tracking. Es lässt sich als App installieren und funktioniert offline.

## Tools

| Tool | Was es macht |
|---|---|
| **Projektstrukturplan (PSP)** | Projekt in Phasen, Teilaufgaben und Arbeitspakete gliedern. Die PSP-Codes (1, 1.1, 1.1.2 …) werden automatisch vergeben. Darstellung als Mischform oder Baum. |
| **Gantt-Diagramm** | Zeitplan mit Tages-, Wochen- und Monatsansicht, Abhängigkeiten, Gesamtpuffer, kritischem Pfad, Meilensteinen, Fortschritt und Heute-Linie. Wochenenden und Feiertage werden übersprungen. |
| **Netzplan** | Vorgangsknotennetzplan mit Vorwärts- und Rückwärtsrechnung (FAZ, FEZ, SAZ, SEZ, GP, FP). Der kritische Pfad wird hervorgehoben. |
| **Risikomatrix** | 5 × 5-Matrix aus Eintrittswahrscheinlichkeit und Auswirkung, mit Risikoliste, Strategie, Maßnahme, Verantwortlichen, Status und Restrisiko. |
| **Kosten und Wirtschaftlichkeit** | Personalkosten direkt aus dem Plan (Dauer × Stunden pro Tag × Stundensatz), Arbeitsplatz-, Sach- und Fremdkosten, jährlicher Nutzen, statische Amortisationsrechnung mit Diagramm und gewichtete Nutzwertanalyse zum Vergleich von Varianten. |
| **Diagramme (UML und ER)** | Anwendungsfall- und Aktivitätsdiagramme sowie ER-Diagramme nach Chen (Entitäten, Beziehungen, Attribute, Kardinalitäten) und in Krähenfuß-Notation (Tabellen mit PK/FK). Eine Prüfung zeigt typische Fehler in der Notation. |
| **PDF-Editor** | Beliebige PDFs öffnen, vorhandene Textzeilen bearbeiten und Text, Notizen, Stift- und Textmarker-Striche, Markierungen, Rechtecke, Ellipsen, Linien, Pfeile, Bilder, Stempel und die eigene Unterschrift einfügen oder Stellen abdecken. Alles bleibt auswählbar, verschiebbar, skalierbar und drehbar, mit Eigenschaften-Panel für Farben, Füllung, Deckkraft, Linienart, Schrift und Bildanpassungen. Pixel- und Objekt-Radierer. Seiten verschieben, drehen, duplizieren, einfügen oder löschen. Speichern als PDF oder Word. |
| **Speichern als** | Export als PDF, Word (.docx), PNG, SVG, HTML-Bericht oder JSON-Projektdatei. |
| **Meine Projekte** | Mehrere Projekte nebeneinander verwalten, duplizieren, als Datei sichern oder wieder laden. |

Alle Pläne nutzen dieselben Daten. Eine Änderung in einer Ansicht ist sofort in allen anderen sichtbar.

## Funktionen

- **Direkt im Diagramm bearbeiten.** Doppelklick benennt um, Ziehen verschiebt, die Balkenkante ändert die Dauer, ein Griff verknüpft Vorgänge, Rechtsklick zeigt alle Aktionen.
- **Diagramm-Editor:** Einrasten an der Mitte und Hilfslinien halten Linien gerade, verschiebbare Ankerpunkte ändern den Linienverlauf, Linienenden lassen sich umhängen, und jedes Element hat eigene Füllfarbe, Textfarbe, Schriftgröße, Fett/Kursiv, Ausrichtung und Linienart. Strg+Umschalt+C/V überträgt ein Format.
- **Touch:** ein Finger verschiebt, zwei Finger zoomen, langes Drücken öffnet das Menü.
- **Lesbarer PDF-Export.** Eine Mindestschriftgröße wird eingehalten. Große Pläne werden auf mehrere Seiten verteilt, und die Schnitte liegen zwischen den Elementen, damit keine Box halb abgeschnitten wird.
- **Anordnungsbeziehungen** EA, AA, EE und AE, mit Zeitabstand in Tagen.
- **Vorlagen**: leeres Projekt, Beispiel Ticketsystem, IHK-Abschlussprojekt, Website, Veranstaltung.
- **Hell- und Dunkelmodus**, einstellbare Akzentfarbe und Schriftgröße.
- **Deutsch und Englisch.**
- **Tastenkürzel.** In der App zeigt `?` die vollständige Liste.
- **Menüleiste** (Datei, Bearbeiten, Ansicht, Fenster, Hilfe) wie in Desktop-Programmen.
- **Andockbare, verstellbare Seitenleiste und Panels.**

## Loslegen

**Online:** den GitHub-Pages-Link des Repositorys öffnen. In Chrome oder Edge dann unter *Einstellungen → App → Installieren*, auf dem iPhone über *Teilen → Zum Home-Bildschirm*.

**Offline als Einzeldatei:** `docs/projectkit.html` direkt von der Festplatte öffnen. Darin steckt alles, was die App braucht.

## Auf GitHub Pages hosten

1. Repository auf GitHub hochladen.
2. Unter *Settings → Pages* die Option *Deploy from a branch* wählen, Branch `main`, Ordner `/docs`.
3. Nach etwa einer Minute ist die App online und installierbar.

## Entwicklung

Der Quellcode liegt aufgeteilt in `src/`. Der Build fügt alles zu einer Datei zusammen und braucht nur Node.js:

```
node build.js
```

| Pfad | Inhalt |
|---|---|
| `src/index.html` | Markup, lädt die CSS- und JS-Dateien in Reihenfolge |
| `src/css/` | Styles, eine Datei pro Bereich |
| `src/js/` | App-Code, nummeriert in Ladereihenfolge (Kern, Sprache, Modell, Ansichten, Diagramme, Kosten, Export, Speicher …) |
| `src/vendor/` | Eingebettete Bibliotheken |
| `src/icons/` | App-Icons |
| `docs/` | Build-Ergebnis: `index.html` (PWA mit Service Worker und Manifest) und `projectkit.html` (Einzeldatei) |
| `test/smoke.py` | Playwright-Rauchtest: `python3 test/smoke.py docs/projectkit.html` |

Beim Entwickeln kannst du `src/index.html` auch direkt ohne Build öffnen.

## Wo sind meine Daten?

Alles wird automatisch in deinem eigenen Browser gespeichert, in localStorage und zusätzlich in IndexedDB. Auch die Einstellungen werden gespeichert, inklusive welche Hinweise du schon geschlossen hast. Nichts wird irgendwohin hochgeladen.

- Jeder Browser und jedes Gerät hat eigene Daten. Mit *Meine Projekte → Alle als Datei sichern* nimmst du Projekte auf ein anderes Gerät mit.
- In privaten Fenstern und beim Löschen der Browserdaten gehen die Projekte verloren. Wichtige Projekte deshalb zusätzlich als Datei sichern.

## Verwendete Bibliotheken

Diese Bibliotheken sind eingebettet, deshalb funktioniert die App ohne Internet:

- [pdf-lib](https://github.com/Hopding/pdf-lib) 1.17.1 · MIT
- [PDF.js](https://github.com/mozilla/pdf.js) 3.11.174 · Apache 2.0
- [JSZip](https://github.com/Stuk/jszip) 3.10.1 · MIT
