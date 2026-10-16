 Evaluation – Lauf Prompt V3 (Copilot-Fragebogen)
 
## 1. Metadaten
 
| Feld | Angabe |
|---|---|
| Evaluierter Lauf | Fragebogen „Akzeptanz der geplanten Nutzung von Microsoft Copilot“ (Word-Datei, Stand 15.10.2026) |
| Erzeugender Prompt | Promt Version 3 (Projektdokument) |
| Erzeugendes Modell | nicht dokumentiert |
| Gutachten erstellt | 15.10.2026, Gutachter-Prompt „Unabhängige Gutachterin für Fragebogenkonstruktion“ (Kriterien 0, A–D) |
| Gutachtendes Modell | claude-opus-5-5 (konfiguriert) |
| Prüfgrundlage | D1 Itemkatalog; P2 Wichmann et al. (2025); P3 Paetow et al. (2026); S2 Sindermann et al. (2021) |
| Fall | Microsoft Copilot · Beschäftigte ohne KI-Fachausbildung · vor der Einführung · Akzeptanz der geplanten Nutzung |
 
## 2. Ergebnis auf einen Blick
 
| Kennzahl | Wert |
|---|---|
| Geprüfte Items | 34 (RAA 15 · TTF 14, davon 4 TC-Filter · ATAI 5) |
| Geprüfte Hypothesen | 7 |
| Befunde gesamt | 17 |
| davon schwer | 2 |
| davon mittel | 5 |
| davon gering | 10 |
| Nicht vorhandene Elemente | Instruktion (Anonymitätshinweis, neutrale Beschreibung), Copilot-Einführungstext – nicht geprüft |
 
### Befunde je Kriterium und Schwere
 
| Kriterium | schwer | mittel | gering | gesamt |
|---|---|---|---|---|
| 0 Quellenechtheit | 0 | 0 | 0 | 0 |
| A Theorievermischung | 2 | 2 | 0 | 4 |
| B Double-Barreled | 0 | 0 | 0 | 0 |
| C Suggestivität/Verständlichkeit | 0 | 0 | 5 | 5 |
| D Quellenangaben | 0 | 3 | 5 | 8 |
| **Summe** | **2** | **5** | **10** | **17** |
 
### Stärken des Laufs
 
- Alle 34 Item-IDs existieren im Katalog; alle Originalitems stimmen wörtlich überein; alle Konstruktzuordnungen sind korrekt.
- Keine Double-Barreled-Items.
- Regel „ein Konstrukt = eine Quelle = eine Theorie“ auf Itemebene eingehalten; Ausschlüsse (UTAUT2/SET aus P2, P4, P5, P1, MAILS) begründet.
- Eigene Einschätzungen überwiegend mit [eigene Bewertung] gekennzeichnet; offene Punkte (Skala, Filter, Ergebnisvariable H6/H7, Technologiebeschreibung) selbst benannt.
 
### Wichtigste Schwäche
 
Die Theorietrennung wurde auf Itemebene, aber nicht auf Hypothesenebene durchgesetzt: H6/H7 haben kein gemessenes Kriterium, H5 verbindet TTF unerkannt mit UTAUT (BI laut P3 aus Venkatesh et al., 2003).
 
## 3. Befundliste mit Ursachenanalyse
 
Spalte „Ursache in V3“: fehlende oder unklare Regel im erzeugenden Prompt. Spalte „Abdeckung in Prompt_V4“: [eigene Bewertung] anhand des Projektdokuments Prompt_V4 (ja / teilweise / nein).
 
| Nr. | Krit. | Fundstelle | Befund (Kurzform) | Schwere | Ursache in V3 | Abdeckung in Prompt_V4 |
|---|---|---|---|---|---|---|
| 1 | A | H6, H7 | Kriterium „Nutzungsbereitschaft Copilot“ nicht gemessen; Hypothesen nicht prüfbar | schwer | Keine Regel, dass Prädiktor und Kriterium mit Items gemessen werden | ja |
| 2 | A | H5; P3-BI1–3 | BI laut P3 aus UTAUT (Venkatesh et al., 2003), als TTF geführt; Brückenhypothese nicht gekennzeichnet | schwer | Keine Regel zur Theorieherkunft laut Methodenteil; keine Regel zu Brückenhypothesen | nein |
| 3 | A | P3-TC/TTF (8 Items) | 4 von 8 Aufgabenarten mit je 1 statt 3 Items; TTF-Aggregation der Quelle (Mittelwert relevanter Items) nicht übernommen | mittel | „3–4 Items je Konstrukt“ ohne Regel zur Messstruktur der Quelle | teilweise (Filter ja, Aggregation nein) |
| 4 | A | P2-PN1, PN2 | Kontext „bei der Arbeit“ macht Freunde/Familie als Bezugsgruppe kaum urteilsfähig | mittel | Keine Grenze für Kontextadaptionen (Bezugsgruppen/-ebene) | teilweise |
| 5 | D | Definitionen RAA | Definitionen als „nicht enthalten“ angegeben, stehen aber in P2, Tab. 1 | mittel | Definition nicht als Ausgabe gefordert; keine Pflicht zur Volltextsuche vor „nicht in den Quellen enthalten“ | teilweise (Definition mit Seite gefordert) |
| 6 | D | Definitionen TTF, ATAI | Nur Theorie- bzw. Strukturbeschreibung, keine Konstruktdefinitionen (PERF, BI, Acceptance, Fear) | gering | wie Nr. 5 | ja |
| 7 | D | Antwortskala | Umstellung auf 1–5 dokumentiert, nicht begründet; S2 wählte 11 Stufen bewusst; Auswertung von „kann ich nicht beurteilen“ offen | mittel | Skala vorgegeben ohne Dokumentations-/Begründungspflicht | teilweise (Doku + Codierung, keine Begründung) |
| 8 | D | S2-05 | Schwache Ladung (DE 0.42); S2 überlässt Aufnahme der Stichprobenentscheidung – Begründung fehlt | mittel | Keine Regel zu itembezogenen Hinweisen der Quelle | nein |
| 9 | D | S2-01/03/05 (R)* | Optionaler ATAI-Gesamtwert nicht durch S2 gedeckt | gering | Polungsregel (R) ohne Bezug zur validierten Skalenbildung | ja |
| 10 | D | H3 | Hypothesennummer „nicht enthalten“ – tatsächlich P2, H10 (β = −.218) | gering | Keine Pflicht zu H-Nr. und Ergebnis | ja |
| 11 | D | H1, H2, H4, H5 | β-Werte aus integrierten Modellen ohne Hinweis auf eingeschränkte Übertragbarkeit | gering | Keine Regel zur Kennzeichnung von Modellabweichungen | nein |
| 12 | D | Literatur | Sekundärzitate ohne „zit. n.“; Literaturverzeichnis nur Kurzangaben, nicht APA 7 | gering | Kein Literaturverzeichnis gefordert | teilweise („zit. n.“ ja, Verzeichnis nein) |
| 13 | C | P2-BI1/2, P3-BI1/2 | „Ich würde planen/beabsichtigen“ mehrdeutig; P3-Original bereits Indikativ | gering | „Zukünftige Nutzung im Konjunktiv“ pauschal | nein |
| 14 | C | P2-ATT4 | „angenehm“ gibt „enjoyable“ ungenau wieder | gering | Keine Vorgabe zur Übersetzungsgenauigkeit | nein |
| 15 | C | P2-BI3, P2-PBC4 | Verstärker aus Original („definitely“, „really“) – beibehalten, Begründung über Validierung | gering | Keine Regel zum Umgang mit Verstärkern im Original | teilweise |
| 16 | C | Blöcke RAA, TTF | Nur gleich gepolte Items – beibehalten, Akquieszenz als Limitation | gering | Keine Regel zu Polung/Limitationen | nein |
| 17 | C | P2-BI / P3-BI | Nahezu identische Intentionsitems zweimal vorgelegt | gering | Keine Regel zu Redundanz zwischen Theorieblöcken | teilweise |
 
## 4. Abgeleitete Prompt-Regeln (Priorität)
 
1. **Hypothesen:** Prädiktor und Kriterium mit Item-IDs im Fragebogen nachweisen; sonst Hypothese streichen. (Nr. 1)
2. **Theorieherkunft:** aus dem Methodenteil der Quelle („items adapted from …“), nicht aus Titel oder Gesamtmodell; theorieübergreifende Hypothesen als Brückenhypothese mit Quellenbeleg. (Nr. 2)
3. **Messstruktur:** Unterbereiche, Filter und Aggregation der Quelle vollständig übernehmen; Kürzungen als Abweichung begründen. (Nr. 3)
4. **Definitionen:** je Konstrukt mit Fundstelle; „nicht in den Quellen enthalten“ erst nach Prüfung von Tabellen, Methodenteil und Anhang. (Nr. 5, 6)
5. **Skala:** Abweichung je Instrument dokumentieren und begründen; Auswertung von „kann ich nicht beurteilen“ festlegen. (Nr. 7)
6. **Hypothesenquelle:** H-Nr., β, p, Ergebnis; Hinweis bei integrierten Modellen. (Nr. 10, 11)
7. **Formulierung:** Absichtsverben im Indikativ mit Zeitbezug; bedeutungsgenaue Übersetzung; Verstärker nur aus validiertem Original mit Begründung. (Nr. 13–15)
8. **Literatur:** vollständiges APA-7-Verzeichnis, Sekundärzitate „zit. n.“. (Nr. 12)
 
## 5. Nächster Schritt
 
Prompt_V4 deckt Nr. 2, 8, 11, 13, 14 und 16 nicht ab [eigene Bewertung]. Diese Punkte im nächsten Prompt-Stand prüfen und einen neuen Lauf mit demselben Fall gegen dieselben Kriterien (0, A–D) evaluieren, um Befundzahlen vergleichen zu können.
