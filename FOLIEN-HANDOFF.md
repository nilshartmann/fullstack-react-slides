# Folien-Handoff — „Fullstack React mit TanStack Start"

> Zusammenfassung der Folien-Arbeit aus Claude-Session `2e324d2c` (31.05.2026) als
> Start-Kontext für eine **neue Session**, in der wir die Folien weiter diskutieren.
>
> ⚠️ **Wichtig:** Die `.pptx` wurde nach der Session noch mehrfach von Hand
> überarbeitet. Dieses Dokument ist **historischer Kontext + offene Punkte**, nicht
> der Ist-Stand. Der echte Stand ist immer die Datei
> `fullstack-mit-tanstack-start.pptx` — die zuerst lesen.

## Rahmen des Talks

- **Titel:** Fullstack React mit TanStack Start
- **Slot:** 45 Min **inkl. Theorie**. Theorie hart auf **max. ~10 Min** deckeln,
  damit für die 8 Live-Demo-Schritte (~4 Min/Schritt) Zeit bleibt.
- **Publikum:** React-Kenntnisse vorausgesetzt. **TanStack Query** als bekannt
  annehmen (nur kurz „globaler Cache" antippen). **RSC in der Theorie NICHT
  erklären** — RSC ist die Pointe, die erst die Live-Demo (#04) einlöst.
- **Demo-App:** hütly (separates Repo `huetly-beispiel-app/huetly`). Die Folien
  liegen bewusst in **diesem** eigenen Repo (`fullstack-react-slides`).
- **Aktueller Demo-Code:** Der `main`-Branch von hütly ist nur der INITIAL-Stand.
  Die **vollständige, fertige Live-Demo** (alle Schritte) liegt im dauerhaften
  `schritte`-Worktree: `../huetly-beispiel-app/huetly-worktrees/schritte`. Wenn in
  einer Slides-Session der echte Demo-Code gebraucht wird, diesen Worktree per
  `/add-dir ../huetly-beispiel-app/huetly-worktrees/schritte` dazuholen.

## Werkzeug-Hinweis (PPTX-Bearbeitung)

- `.pptx`-Bearbeitung via `python-pptx` (venv im huetly-Repo unter `.venv/`).
- **Grenze:** Animations-Builds (Klick-Animationen) und das **Zusammenlegen** von
  Folien macht Nils selbst in PowerPoint — `python-pptx` zerschießt die Animationen.
  Claude schreibt nur Inhalte/TODOs, legt/löscht ganze Folien, hängt Notizen an.
- **Backups:** Vor jeder Bearbeitung ein Backup. Im Verzeichnis liegen mehrere
  ungetrackte Arbeitskopien (`…copy*.pptx`, `…backup.pptx`) — aufräumen, sobald der
  Stand sitzt; sie blähen das Verzeichnis auf.

## TODO-Marker-System in den Folien

Notizen unten auf den Folien, farbcodiert:

- 🔧 **rot** — inhaltliche TODOs
- ✂️ **blau** — Straffungs-Hinweise (Folien zusammenlegen / kürzen)
- 💡 **grün** — Nachschärfungen / Feinschliff

## Was in der Session passiert ist

Ausgangsdatei: 39 Folien, erkennbar **zwei Vorträge zusammengeworfen** (deutsch/
englisch), viele Animations-Builds.

1. **Gelöscht** (39 → 26 Folien): Next.js-Block (7 Folien) und die redundante zweite
   Quelle (8 engl. Query-/Router-Detailfolien + Toolstack-Dublette).
2. **Neu als Platzhalter eingefügt:**
   - **Scharnier-Folie** „Geht beides? — Bestes aus beiden Welten?" (Übergang Teil 1 → Teil 2)
   - **Roadmap-Folie** „Unsere Demo: hütly Schritt für Schritt auf den Server"
     (letzte Theorie-Folie vor der Live-Demo)
3. Nils hat danach selbst überarbeitet (→ 28 Folien, echte Titel-/Sprecherfolie).
4. **Architektur-Teil gestrafft** von 12 auf ~8 Folien, gegliedert in **4 Beats**.

## Die dramaturgische Leitidee (NICHT verwässern)

Roter Faden: **„Wo läuft der Code / wie kommt JS in den Browser?"**

- **Das „Bundle-Saatkorn" / der Cliffhanger:** „JS nur dort, wo es gebraucht wird"
  wird in Teil 1 als **Wunsch** gelegt, **nicht** als gelöst verkauft. Eingelöst wird
  er erst in der Live-Demo **#04 (RSC)**.
- **SSR-Grenze ehrlich benennen:** SSR von SPAs rendert einmal vor und hydriert —
  **das ganze JS-Bundle** geht trotzdem in den Browser, auch für nie-interaktive
  Teile. Genau das ist die RSC-Motivation. Folien dürfen das nicht vorwegnehmen.

## Teil 1 — Architektur-Herführung (4 Beats, ~8 Folien)

- **Beat 1 — Klassische serverseitige Apps** (Java/Express/.NET): Stärke = fertige
  Seite sofort, JS nur wo nötig ❤️. Leitfrage als Überschrift: **„Warum nicht einfach
  dabei bleiben?"** → Antwort: jede Interaktion = Roundtrip **+** bunter Tech-Strauß.
- **Beat 2 — SPA als Gegenmodell:** alles JS im Browser → maximal interaktiv, eine
  Codebasis. Preis: viel JS, blockiert First Paint, statische Inhalte brauchen kein JS.
- **Beat 3 — SSR von SPAs ≠ klassisches SSR** (für gemischtes/Backend-Publikum
  kritisch): vorgerendert + hydriert, **bleibt aber eine SPA**; nicht „HTML pro
  Request mit Roundtrips". Diese Abgrenzung muss explizit auf die Folie.
- **Beat 4 — Fullstack verbindet beide Welten** → Brücke zu TanStack Start
  (eine Codebasis + SSR out-of-the-box).

## Offene Folien-TODOs (Stand Session-Ende)

- **F11** 💡 — Abgrenzung „SSR ≠ klassisches SSR" explizit auf die Folie schreiben.
- **F12** 💡 — „JS nur wo nötig" NICHT als gelöst zeigen; als Cliffhanger staffeln
  („eine Codebasis gibt's gleich; JS nur wo nötig kommt später = RSC"). Formulierung
  „SSR lädt trotzdem das **ganze** JS" (konsistent zu Beat 2).
- **RSC-Folie** 🔧 — sagt aktuell „experimentell / kein RSC". Faktischer Fehler,
  widerspricht dem Talk-Kern → muss raus/korrigiert.

## Nächster Arbeitsblock (noch NICHT gemacht)

**Teil 2 („TanStack", Tech-Stack-Folien) entrümpeln:**
- Animationsreste bereinigen („RC", doppeltes „Isolated").
- Botschaft „**Query ist orthogonal**" sauber rausstellen.
- Ankerbild „**Start = Router + SSR**".
- RSC-Folie korrigieren (s. o.).

## Bezug Theorie ↔ Live-Demo

- Die **Markdown-Description** in der `PostDetailCard` ist der greifbare RSC-Beweis:
  `react-markdown` + `remark-gfm` (100 KB+) bleiben bei #05a server-seitig → messbarer
  Bundle-Unterschied. (In der App bereits umgesetzt.) Auf den Folien den Bogen
  Theorie → Demo entsprechend vorbereiten.

---

## Hand-off-Prompt für die neue Session

> Kopiervorlage — in einer neuen Session starten, die im Slides-Repo läuft
> (`fullstack-react-slides/`):

```
Ich möchte an den Folien für meinen Talk „Fullstack React mit TanStack Start"
weiterarbeiten. Lies zuerst FOLIEN-HANDOFF.md in diesem Verzeichnis — das ist der
Kontext und die offenen Punkte aus einer früheren Session. Lies danach den
AKTUELLEN Stand der Folien aus fullstack-mit-tanstack-start.pptx (das venv mit
python-pptx liegt im Nachbar-Repo unter huetly-beispiel-app/huetly/.venv/ —
Aufruf: ../huetly-beispiel-app/huetly/.venv/bin/python <script>).

Wichtig: Die .pptx wurde nach der Handoff-Session noch von Hand überarbeitet, also
ist die Datei maßgeblich, nicht das Handoff-Dokument. Animations-Builds und das
Zusammenlegen von Folien mache ich selbst in PowerPoint — du schreibst Inhalte/TODOs
und legst/löschst ganze Folien. Mach vor Änderungen ein Backup.

Gib mir zuerst einen Abgleich: Wie unterscheidet sich der aktuelle .pptx-Stand vom
Handoff? Welche der offenen TODOs sind schon erledigt? Dann besprechen wir als
Nächstes Teil 2 (TanStack-Tech-Stack-Folien) entrümpeln.
```
