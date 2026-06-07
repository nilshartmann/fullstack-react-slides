# Slides-Repo — Foliendecks für Vorträge

Dieses Repo enthält die PowerPoint-Decks von Nils' Vorträgen. **Aktiv bearbeitet**
wird derzeit das Deck zum Talk **„Fullstack React mit TanStack Start"**:
`fullstack-mit-tanstack-start.pptx` (im Repo-Root). Ältere Decks liegen in `Material/`.

Bewusst ein **eigenes** git-Repo, getrennt von der Demo-App: `.pptx` sind große
Binärdateien, die die git-History aufblähen, und das öffentliche Export-Repo der
App soll ohne Folien bleiben.

## PPTX bearbeiten

- Werkzeug: `python-pptx` im venv des Nachbar-Repos:
  `../huetly-beispiel-app/huetly/.venv/bin/python <script>`.
- **Vor jeder Änderung ein Backup** der `.pptx` anlegen.
- **Grenze:** Animations-Builds (Klick-Animationen) und das **Zusammenlegen** von
  Folien macht Nils selbst in PowerPoint — `python-pptx` zerschießt die Animationen.
  Claude schreibt Inhalte/TODOs, legt/löscht ganze Folien, hängt Notizen an.
- Arbeitskopien (`…copy*.pptx`, `…backup.pptx`) aufräumen, sobald der Stand sitzt.

## TODO-Marker auf den Folien

- 🔧 **rot** — inhaltliche TODOs
- ✂️ **blau** — Straffungs-Hinweise (Folien zusammenlegen / kürzen)
- 💡 **grün** — Nachschärfungen / Feinschliff

## Demo-Code (anderes Repo)

Die Demo-App hütly liegt unter `../huetly-beispiel-app/huetly`. Deren `main`-Branch
ist nur der INITIAL-Stand; die **vollständige, fertige Live-Demo** (alle Schritte)
liegt im dauerhaften `schritte`-Worktree:
`../huetly-beispiel-app/huetly-worktrees/schritte`. Wird der echte Demo-Code zum
Abgleich mit den Folien gebraucht, diesen Worktree dazuholen:
`/add-dir ../huetly-beispiel-app/huetly-worktrees/schritte`.
