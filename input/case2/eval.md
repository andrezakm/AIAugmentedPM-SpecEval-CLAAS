# Eval: Feature Backlog Prioritizer

**Datum:** 2026-06-09
**Basis:** input/case2/spec.md

---

## Anleitung

PASS = Bedingung ist erfüllt. FAIL = nicht erfüllt. UNKLAR = nicht aus Code oder Output entscheidbar.

## Kriterien

| ID | Kriterium | Wie testen | Pass-Bedingung | Ergebnis |
|----|-----------|------------|----------------|----------|
| E1 | App öffnet fehlerfrei | `prototype/case2/app.html` per Doppelklick im Browser öffnen, Konsole (DevTools) prüfen | Keine Konsolenfehler, Inhalt sichtbar | — |
| E2 | Alle 12 Features sichtbar (keine Filter gesetzt) | App öffnen, alle Filter-Optionen ausgewählt | Tabelle zeigt genau 12 Zeilen | — |
| E3 | Score-Spalte vorhanden und befüllt | Tabelle ansehen | Spalte „score" sichtbar, jede Zeile hat einen numerischen Wert | — |
| E4 | Tabelle nach Score absteigend sortiert | Scores in der Tabelle von oben nach unten vergleichen | Höchster Score oben, niedrigster unten | — |
| E5 | Status-Filter schränkt Anzeige ein | Nur „backlog" auswählen | Nur Features mit status=backlog sichtbar; andere verschwinden | — |
| E6 | Strategischer-Fit-Filter funktioniert | Nur „hoch" auswählen | Nur Features mit strategischer_fit=hoch sichtbar | — |
| E7 | Zähler aktualisiert sich beim Filtern | Filter setzen | Sidebar zeigt korrekte Anzahl sichtbarer Features (z.B. „4 von 12 Features sichtbar") | — |
| E8 | Balkendiagramm vorhanden | App öffnen | Balkendiagramm unterhalb der Tabelle sichtbar, zeigt Feature-Namen und Scores | — |
| E9 | Diagramm spiegelt aktiven Filter | Filter setzen, Diagramm prüfen | Diagramm zeigt nur gefilterte Features — nicht alle 12 | — |
| E10 | Detail-Ansicht erscheint nach Auswahl | Feature aus Selectbox auswählen | Beschreibung und alle Rohwerte des gewählten Features erscheinen unterhalb des Diagramms | — |
| E11 | Keine Daten hardcoded | `data.js` und `app.html` durchsehen (Sichtung) | Kein Feature-Name in `app.html` — Daten kommen ausschließlich aus `data.js` (`window.DATA`) | — |
| E12 | Kein-Treffer-Hinweis bei leerem Ergebnis | Alle Status-Werte abwählen oder Kombination ohne Treffer | Hinweistext erscheint, Tabelle und Diagramm bleiben leer oder zeigen Meldung | — |
