# Spec: Feedback Cluster Viewer

**Version:** 1.0
**Datum:** März 2026
**Basis:** input/case1/brief.md

---

## Zweck

Ein Agent hat die Anforderungen und das Feedback der Stakeholder zu Themen-Clustern zusammengefasst. Die Cluster-Datei ist aber lang und unübersichtlich — NeoEmployee PMs sollen die Ergebnisse schnell sichten und nach Quelle filtern können, ohne die Markdown-Datei von Hand durchzulesen.

## Nutzer

NeoEmployee PMs und Berater:innen, 1–2 Personen, die mit dem Cluster-Ergebnis weiterarbeiten. Technisches Niveau: mittel — keine Programmierkenntnisse nötig.

## Daten-Input

- Datei: `input/case1/data/clusters.md`
- Format: Markdown mit Cluster-Struktur
- Cluster-Struktur: `## Cluster N: [Name]`, darunter Häufigkeit, Zusammenfassung, Belege mit Quellenangabe
- Quellen-Tags in Belegen: slack, email, interview, internal (aus Absender oder Dateiname erkennbar)

## UI-Komponenten

**1. Seitenleiste (Sidebar)**
- Multiselect: "Nach Quelle filtern" — Optionen: Slack, E-Mail, Interview, Intern
- Standardmäßig: alle Quellen ausgewählt
- Anzeige: Anzahl sichtbarer Cluster ("X von Y Clustern")

**2. Hauptbereich — Clusterkarten**
- Eine Karte pro Cluster
- Karte zeigt: Cluster-Name (Überschrift), Häufigkeit, Zusammenfassung
- Unter jeder Karte: aufklappbarer Bereich "Belege" mit Zitaten und Quellenangaben
- Reihenfolge: wie in der Datei

**3. Sonderfall: kein Treffer**
- Wenn Filter keine Cluster ergibt: Hinweistext "Keine Cluster für die gewählten Quellen."

## Constraints

- Kein Backend, kein Server, keine Datenbank, keine API
- Eine `app.html` + `data.js` in `prototype/case1/` — öffnet per Doppelklick im Browser (`file://`)
- Kein Login, keine Authentifizierung
- Kein Schreiben von Daten — nur Lesen
- Daten kommen aus `data.js`, nicht hardcoded in `app.html`
