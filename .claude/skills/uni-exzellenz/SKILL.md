---
name: uni-exzellenz
description: Verbindliche Standards für wissenschaftliches Arbeiten auf 1,0-Niveau – Null-Halluzination, API-verifizierte Quellen, Primärdaten, kritische Argumentation. Verwenden bei Hausarbeiten, Thesen, Literaturrecherche, Essays, empirischen Analysen oder jeder Aufgabe mit Quellen, Zitaten oder Statistiken.
---

# Uni-Exzellenz: Verbindliche Standards

## 1. Null-Halluzinations- & Quellengarantie
- NIEMALS Autoren, Titel, Jahreszahlen, DOIs, Zitierzahlen oder empirische Werte erfinden.
- Bei Terminal-/Web-Zugriff jede Quelle aktiv verifizieren:
  - Semantic Scholar: `curl -s "https://api.semanticscholar.org/graph/v1/paper/search?query=<BEGRIFFE>&fields=title,authors,year,venue,citationCount,externalIds&limit=5"`
  - OpenAlex: `curl -s "https://api.openalex.org/works?search=<BEGRIFFE>&per-page=5"`
  - Crossref (DOI): `curl -s "https://api.crossref.org/works/<DOI>"`
  - Primärdaten: Weltbank (`https://api.worldbank.org/v2/country/<ISO3>/indicator/<CODE>?format=json`, z. B. `SI.POV.GINI`, `NY.GNP.PCAP.CD`), OECD (`https://sdmx.oecd.org/public/rest/`), IMF (`https://www.imf.org/external/datamapper/api/v1/`).
- Abgleich: Autor, Titel, Jahr, Journal, DOI müssen mit dem API-Treffer übereinstimmen.
- Jede nicht per echtem API-Treffer oder DOI-Abruf verifizierte Quelle zwingend markieren: `[QUELLE PRÜFEN + Suchbegriff]`.

## 2. Qualitätsfilter (1,0-Standard)
- **Impact:** Hochzitierte Peer-Review-Artikel aus Q1-Journals und etablierte Grundlagenwerke priorisieren; Citation Count (ungefähr, mit Quelle/Abrufdatum) angeben.
- **Aktualität:** Standardwerke mit Spitzenforschung der letzten 3–5 Jahre kombinieren.
- **Primärquellen-Pflicht:** Empirische Zahlen (Gini, GNI per capita etc.) nie aus Sekundärartikeln, immer direkt aus Primärquelle (World Bank Open Data, OECD, nationale Statistikämter) mit exaktem Erhebungsjahr.

## 3. Akademische Argumentation & Methodik
- Analytisch, kritisch, nuanciert: Gegenpositionen, methodische Limitationen, Kausalitätsprobleme (Endogenität, Selektion, Confounder) darstellen – keine oberflächlichen Zusammenfassungen.
- Strikt trennen: **Empirie** (belegt) | **Theorie/Modell** | **Eigene Einordnung**.
- Jede Tatsachenbehauptung und Zahl sofort im Text belegen (Autor, Jahr, ggf. Seite/Datenbank).

## 4. Token-Sparsamkeit
- Extrem präzise, dicht, ohne Füllwörter, Einleitungen, Floskeln.
- Nur angefragte Dateien ändern; keine unnötigen Beispieldateien.
