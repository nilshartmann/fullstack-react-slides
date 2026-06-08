# Geplante Konferenzen

Der Talk ist aktuell für mehrere unterschiedliche Konferenzen geplant.

Zielpublikum und Inhalt ist leicht anders (bei WDC Inhalt auch ganz anders)

**Aktuell** wird der Talk für Karlsruher Entwicklertag vorbereitet
- Die anderen beiden Konferenzen nur, um die im "Hinterkopf" zu haben

## Karlsruher Entwickertag

- Möglicherweise nicht nur JavaScript/reine Frontend-Entwickler
- Themen:
  - was ist SSR?
  - warum SSR?
  - Überleitung Fullstack / RSC

## EnterJS
- Alle mit JavaScript Know-HOW
- SSR kann als verstanden angenommen werden
  - Eventuell kurze Motivation, warum SSR (nicht offensichtliche Gründe)
- Im Abstract: Unterschiede zu Next.js (!)
  - Deswegen: **Fokus** auf Unterschied zu Next.js (server-first) zu TanStack start (client-first)
  - **Keine historische Herleitung** (klassische Webapp, SSR etc, evtl. Unterschied SSR <-> RSC)


## WDC

- Next.js (!) Talk
- Hier erwarte ich auch Entwickler, die keine Frontend-Spezialisten sind (sondern z.B. Backendler, die auch Frontend machen)
- Aus diesem Talk die SSR herleitung und ggf. RSC herleitung übernehmen. Nicht die Beispiel-Anwendung.


# Inhalte

## Warum nicht klassisch? (Java, PHP. .NET)
**Pro SPA:**
- hoher Bedienkomfort möglich, 
- volle Interaktivität, 
- Benutzungsmuster wie bei Desktop-Aktionen möglich: Drag-n-Drop, partielle Aktualisierungen, schnelles Feedback (z.B. Warte-Indikator nach Button klick), Auto-save von Änderungen, Richt-Text-Editoren etc.
**Pro klassisch**:
- wenig JS
- schnelle erste Darstellung etc.
**Contra klassisch**:
- wenig Interaktion
- aber: für "Webseiten" sehr gut geeignet

**Anwendungsarten**:
- Desktop-like, SPA: Notion, Teams, Miro, Excalidraw
- Mischform (SPA wahrscheinlich): GitHub, Jira, DB-Navigator
- Mischform (vielleicht klassisch möglich, SPA nicht zwingend): unsere anwendung ("Huetly"), eCommerce (Warenkorb, Checkout)
- Tendenziel "Webseite" (kein SPA): Nachrichtenseite (Spiegel, Süddeutsche, kicker)

**Problem**:
- Übergang fließend

### Offen für Talk:
- Warum trägt "klassisch" nicht für "Michform" wie huetly (hier ein Like Button, dort ein Formular), keine große Interaktion?
  - Argumentation in den Slides noch schwach



## SSR

**Grundsätzlich zu SSR**:
- Unterschied SSR bei SPA vs. "klassischem" serverseitigem Rendern (Java, PHP, .NET, ggf. Templatesprache im Backend)


**Gründe für SSR:**

- Bei SSR geht es nicht nur um Geschwindigkeit durch Roundtrips, sondern z.B. auch:
- besseres Caching
- schnellere FCP/LCP
- weniger JS im Browser
- SEO
- Data fetching in der Nähe der Origin (DB/CMS)
- weniger Blockierungen des Seitenladens durch Streaming


