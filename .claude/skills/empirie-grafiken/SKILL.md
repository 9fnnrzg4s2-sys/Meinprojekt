---
name: empirie-grafiken
description: Wissenschaftliche Datenvisualisierungen mit Python für universitäre Arbeiten, empirische Analysen und Publikationen erstellen und überprüfen.
---

# Empirie-Grafiken

## Technologie
- Python mit matplotlib und seaborn; Datenverarbeitung mit pandas/numpy nur soweit nötig.
- Reproduzierbar: ein Skript von Rohdaten bis Grafik, feste Seeds, Datenabrufdatum im Code dokumentiert.
- Keine unnötigen Bibliotheken.

## Grafikqualität
- Publikationsniveau.
- Rastergrafiken mindestens 300 DPI; PDF oder SVG als Vektorformat bevorzugen.
- Achsenbeschriftungen immer mit Einheit (z. B. „BIP pro Kopf (KKP, konst. 2021 int. $)“).
- Lesbare Schriftgrößen (≥ 8 pt bei Druckgröße), nachvollziehbare Legenden.
- Zurückhaltende, barrierearme Paletten (z. B. `seaborn.color_palette("colorblind")`, viridis/cividis); Information nie nur über Farbe kodieren.
- Einheitliches Layout: gleicher Stil, gleiche Schrift, gleiche Größen über alle Grafiken.
- Keine 3D-Darstellungen, Schatten, überladenen Farben oder Effekte.
- Keine irreführenden Skalen: Balkendiagramme ab 0; abgeschnittene oder logarithmische Achsen ausdrücklich kennzeichnen; gleiche Skalen bei Vergleichs-Panels.

Basis-Setup:
```python
import matplotlib.pyplot as plt
import seaborn as sns
sns.set_theme(style="whitegrid", context="paper", palette="colorblind")
plt.rcParams.update({"savefig.dpi": 300, "savefig.bbox": "tight", "pdf.fonttype": 42, "svg.fonttype": "none"})
# fig.savefig("abb1.pdf"); fig.savefig("abb1.png", dpi=300)
```

## Datenqualität
- Ausschließlich nachvollziehbare, verifizierbare Quellen; Primärquellen bevorzugen (Weltbank, OECD, Eurostat, nationale Statistikämter).
- Keine Daten, Quellen, Beobachtungen oder Ergebnisse erfinden. Liegen keine echten Daten vor: keine Grafik mit Platzhalterwerten als Ergebnis ausgeben.
- Fehlende Werte transparent behandeln: nicht stillschweigend interpolieren; Lücken sichtbar lassen oder Methode (Interpolation, Ausschluss) im Text/Quellenzeile nennen; Anzahl fehlender Beobachtungen angeben.
- Transformationen (Log, Indexierung, Deflationierung, Aggregation, Glättung) dokumentieren.
- Keine Kausalität aus Korrelationen ableiten; Beschriftungen und Titel entsprechend neutral formulieren.

## Quellenangaben
Unmittelbar unter jeder Grafik eine Quellenzeile mit:
- Institution/Herausgeber,
- konkretem Datensatz (ggf. Indikatorcode),
- Betrachtungszeitraum,
- URL oder genauer Fundstelle (ggf. Abrufdatum),
- ggf. „eigene Berechnung auf Basis von …“.

Muster: `Quelle: Weltbank, World Development Indicators, Indikator SI.POV.GINI, 2000–2022, https://data.worldbank.org/indicator/SI.POV.GINI (Abruf: TT.MM.JJJJ); eigene Darstellung.`

Fehlt eine verifizierbare Quelle: ausdrücklich kennzeichnen (`Quelle: [NICHT VERIFIZIERT – Quelle prüfen]`). Niemals eine Quelle ergänzen oder erfinden, damit die Grafik vollständig wirkt.

## Prüfcheckliste (bei Überprüfung bestehender Grafiken)
Format/DPI · Achsen + Einheiten · Skalierung · Palette/Barrierearmut · Legende · Quellenzeile vollständig · Datenlücken dokumentiert · keine Kausalbehauptung. Mängel knapp mit konkretem Korrekturvorschlag melden.
