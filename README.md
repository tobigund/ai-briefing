# Tobi’s KI Wochenrückblick

Die wichtigsten KI News der Woche im Überblick, von Tobias Gundermann.
Live: **https://ai-brief.young-growth.com**

## Was die Seite kann

- **Zeitstrahl** aller Ausgaben: eine Spalte pro Kalenderwoche, ein Balken pro Meldung (Länge = Textumfang). Klick oder ← → wechselt die Woche.
- **Archivsuche** über alle Ausgaben, Treffer springen direkt zur Meldung.
- **Themenleiste** pro Ausgabe und **Kompaktansicht** (nur Schlagzeile, Einordnung, Quellen).
- **Deep-Links** pro Ausgabe, z. B. `#2026-kw41`.
- Design nach dem **Glean Design System**, Hell- und Dunkelmodus, mobil nutzbar.

## Wie sie aktualisiert wird

Jeden Sonntag um 9:00 fasst eine Claude-Routine die Ausgaben des „Glean AI Briefing“ der Woche
zusammen, ohne neue Recherche. Die neue Ausgabe kommt als `<section class="edition">` an den Anfang von
`<div id="editions">` in `index.html` und zusätzlich in das claude.ai-Artifact. Zeitstrahl, Suche und Navigation
bauen sich daraus automatisch auf. CSS und Skript bleiben unverändert.

## Hosting

- GitHub Pages aus `main`, Ordner `/`.
- `CNAME`: `ai-brief.young-growth.com`.
- DNS bei Strato: CNAME `ai-brief` → `tobigund.github.io.`, TXT `_github-pages-challenge-tobigund` zur Domain-Verifizierung.
- HTTPS über GitHub (Let’s Encrypt).

Design-Änderungen immer in `index.html` und im Artifact gemeinsam machen, sonst laufen beide Versionen auseinander.
