# Woche 4: Spec, Eval & Prototyp

In dieser Woche lernst du den PM-Kernskill: ein Feature spezifizieren, Abnahmekriterien definieren und einen funktionalen Prototypen bauen — und evaluieren. Du lernst außerdem, einem autonomen System schrittweise mehr Kontrolle zu übergeben.

## So startest du

Kein Python, kein Streamlit, keine Installation. Der Prototyp entsteht als eine einzelne `app.html`, die du per Doppelklick im Browser öffnest.

1. Dieses Repository klonen oder als ZIP herunterladen
2. In VS Code öffnen
3. GitHub Copilot Agent Mode aktivieren
4. Details zum Setup: `SETUP.md`

## Kurs starten

```
/kurs
```

Oder einfach sagen: "starte den Kurs"

## Dateistruktur

| Pfad | Rolle |
|------|-------|
| `CLAUDE.md` | Projekt-Prinzipien, immer aktiv |
| `.claude/skills/kurs/` | Interaktiver Kurspfad (`/kurs`) |
| `.claude/skills/spec-writer/` | Schreibt Spec aus Brief |
| `.claude/skills/eval-writer/` | Schreibt Eval aus Spec |
| `.claude/skills/prototype-builder/` | Baut HTML-Prototyp (`app.html` + `data.js`) aus Spec |
| `.claude/skills/eval-runner/` | Prüft Prototyp gegen Eval-Kriterien |
| `.claude/skills/build-eval/` | Orchestriert Spec → Eval → Prototyp als `/build-eval` |
| `context/` | NeoEmployee-Kontext (company.md, strategy.md) |
| `input/case1/` | Feedback Cluster Viewer — alles vorgegeben |
| `input/case2/` | Feature Backlog Prioritizer — Brief + Daten vorgegeben |
| `prototype/` | Generierte Prototypen (`app.html` + `data.js`) |
| `output/` | Eval-Ergebnisse (entstehen beim Ausführen) |
| `doc/` | Zusatzmaterial |
| `SETUP.md` | VS Code + GitHub Copilot einrichten |

## Modell-Empfehlung

Verwende in GitHub Copilot Agent Mode ein leistungsfähiges Modell. `/build-eval` führt drei Schritte sequenziell aus — ein stärkeres Modell liefert präzisere Specs und lauffähigeren Code.
