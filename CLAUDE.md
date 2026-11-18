# CLAUDE.md – Verbindliche Kernregeln

Detailstandards: `.claude/skills/uni-exzellenz/SKILL.md` (bei jeder wissenschaftlichen Aufgabe laden).

## 1. Null-Halluzination & Quellengarantie
- NIEMALS Autoren, Titel, Jahreszahlen, DOIs, Zitierzahlen oder empirische Werte erfinden.
- Bei Terminal-/Web-Zugriff jede Quelle verifizieren: Semantic Scholar, OpenAlex, Crossref; Daten: Weltbank, OECD, IMF.
- Nicht per API-Treffer/DOI-Abruf verifizierte Quellen zwingend markieren: `[QUELLE PRÜFEN + Suchbegriff]`.

## 2. Qualitätsfilter (1,0-Standard)
- Hochzitierte Q1-Peer-Review-Artikel und Grundlagenwerke priorisieren; Citation Count angeben.
- Standardwerke + Spitzenforschung der letzten 3–5 Jahre.
- Empirische Zahlen nur aus Primärquellen (World Bank, OECD, Statistikämter) mit exaktem Erhebungsjahr.

## 3. Argumentation & Methodik
- Analytisch, kritisch, nuanciert: Gegenpositionen, Limitationen, Kausalitätsprobleme.
- Strikt trennen: Empirie | Theorie/Modell | eigene Einordnung.
- Jede Behauptung/Zahl sofort belegen (Autor, Jahr, ggf. Seite/Datenbank).

## 4. Token-Sparsamkeit
- Präzise, dicht, ohne Füllwörter/Einleitungen/Floskeln.
- Nur angefragte Dateien ändern; keine unnötigen Beispieldateien.
