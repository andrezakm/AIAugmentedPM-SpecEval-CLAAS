# Brief: Feedback Cluster Viewer

**Datum:** März 2026
**Autor:** NeoEmployee PM-Team

---

## Das Problem

Ein Agent hat das gesammelte Feedback und die Anforderungen unserer Stakeholder zu Themen-Clustern zusammengefasst. Das Ergebnis liegt als Markdown-Datei vor — `clusters.md`, mit allen identifizierten Feedback-Clustern.

Das Problem: ab 4 Clustern wird die Datei unübersichtlich. Wir scrollen, suchen, verlieren den Überblick. Es gibt keine Möglichkeit zu filtern — zum Beispiel "zeig mir nur Cluster die auf Slack-Nachrichten basieren" oder "welche Cluster kommen aus Kundeninterviews?".

Heute öffnen wir die Datei im Editor und lesen von oben nach unten. Das kostet Zeit und macht Vergleiche schwer.

## Die Nutzer

NeoEmployee PMs und Berater:innen, die mit dem Cluster-Ergebnis weiterarbeiten. Typisch: 1–2 Personen, die ein Kunden-Briefing vorbereiten oder eine Produktentscheidung treffen wollen.

## Was wir brauchen

Eine einfache lokale App die `clusters.md` einliest und die Cluster übersichtlich darstellt. Filterbar nach Quelle. Keine Datenbank, kein Login, kein Deployment — läuft lokal im Browser, ohne Installation.

## Was wir nicht brauchen

- Kein Backend, keine API
- Keine Benutzerkonten
- Kein schickes Design — Funktion vor Form
- Keine Bearbeitung der Daten — nur Lesen und Anzeigen
