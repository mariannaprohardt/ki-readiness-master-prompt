# Claude_Lauf5_Evaluation

## 1. Metadaten

| Feld | Angabe |
|---|---|
| Evaluierter Lauf | Fragebogen „Akzeptanz Microsoft Copilot (vor Einführung)“ (Word-Datei, Stand 15.10.2026) |
| Erzeugender Prompt | Prompt V5 (Projektdokument) [eigene Bewertung: aus dem Chatverlauf abgeleitet] |
| Erzeugendes Modell | NotebookLM (laut Dateiname); Version nicht dokumentiert |
| Gutachten erstellt | 15.10.2026, Gutachter-Prompt „Unabhängige Gutachterin für Fragebogenkonstruktion“ (Kriterien 0, A–D) |
| Gutachtendes Modell | claude-opus-5-5 (konfiguriert) |
| Prüfgrundlage | D1 Itemkatalog (Questionnaire 3); P3 Paetow et al. (2026); S2 Sindermann et al. (2021); bibliografische Angaben zusätzlich an P2, S1b |
| Fall | Microsoft Copilot · Beschäftigte ohne KI-Fachausbildung · vor der Einführung · Akzeptanz der geplanten Nutzung |

## 2. Ergebnis auf einen Blick

| Kennzahl | Wert |
|---|---|
| Geprüfte Items | 35 (TC 12 · TTF 12 · BI 3 · PERF 3 · ATAI 5) + 5 Itemstämme, Instruktion, Technologiebeschreibung, 8 Literaturangaben |
| Geprüfte Hypothesen | 2 |
| Befunde gesamt | 12 |
| davon schwer | 0 |
| davon mittel | 4 |
| davon gering | 8 |
| Nicht vorhandene Elemente | keine |

### Befunde je Kriterium und Schwere

| Kriterium | schwer | mittel | gering | gesamt |
|---|---|---|---|---|
| 0 Quellenechtheit | 0 | 0 | 0 | 0 |
| A Theorievermischung | 0 | 1 | 1 | 2 |
| B Double-Barreled | 0 | 0 | 0 | 0 |
| C Suggestivität/Verständlichkeit | 0 | 1 | 3 | 4 |
| D Quellenangaben | 0 | 2 | 4 | 6 |
| **Summe** | **0** | **4** | **8** | **12** |

### Stärken des Laufs

- Alle 35 Itemwortlaute und Konstruktzuordnungen stimmen mit D1 bzw. S2 (Tab. 1) überein; alle Seitenangaben zu P3 und S2 sind korrekt.
- Keine Double-Barreled-Items: Creativity-1/-3 (TC und TTF) sind begründet beibehalten („bestehende oder neue“ deckt alle Anforderungen ab; „ohne sie sofort zu bewerten“ ist Kern der McGrath-Definition, S. 320; TC-Subskala validiert, S. 323).
- H1 und H2 stammen aus einer Theorie; beide Kriterien werden gemessen; keine Brückenhypothese; ATAI wird nicht mit TTF-Skalen zusammengefasst.
- Abweichungen von der Quelle sind überwiegend dokumentiert und mit [eigene Bewertung] gekennzeichnet.

### Wichtigste Schwäche

Ein Ausschluss, den die Quelle für ein anderes Konstrukt (TC als Prädiktor) und eine andere Technologie (VR) getroffen hat, wurde auf TTF für Copilot übertragen. Dadurch fehlen genau die Aufgabenarten, für die Copilot laut eigener Beschreibung eingesetzt wird. Ursache ist eine falsch angewendete Quellenstelle, kein bloßer Regelverstoß.

## 3. Befundliste mit Ursachenanalyse

Spalte „Ursache in V5“: fehlende oder unklare Regel im erzeugenden Prompt. Spalte „Abdeckung in V6“: [eigene Bewertung] anhand des Projektdokuments „Prompt V6 – Inventar und Fragebogen“ (ja / teilweise / nein).

| Nr. | Krit. | Fundstelle | Befund (Kurzform) | Schwere | Ursache in V5 | Abdeckung in V6 |
|---|---|---|---|---|---|---|
| 1 | A | TTF-* (Aggregation) | TTF nur über 4 statt aller relevanten Aufgabenarten (P3, S. 323); Einsatzfelder von Copilot (Texte, Zusammenfassungen, Auswertungen) nicht abgedeckt | mittel | Regel „Validierter Umfang“ ohne Geltungsbereich; Teilauswahl „mit der Quelle begründet“ ohne Prüfung des betroffenen Konstrukts | ja (Aggregation mit allen Teilbereichen; Abdeckung der Einsatzfelder) |
| 2 | D | Tab. A „Validierter Umfang“; Aggregation | Begründung mit S. 323 trägt nicht: Ausschluss betrifft TC-Indikatoren (Prädiktor), nicht TTF | mittel | Begründungspflicht ohne Zitatpflicht und ohne Bezugsprüfung | ja (Regeln 3, 4; typischer Fehler) |
| 3 | D | S2-ATAI01–05 | Skala 0–10 → 1–5 ohne tragenden Grund; S2 begründet 11 Stufen ausdrücklich (S. 112); α DE .65/.66 (S. 114) | mittel | „Begründung aus der Quelle, falls sie andere Skalierungen zulässt“ zu weich | ja (2.5) |
| 4 | C | Instruktion, Ablauf Pkt. 4 | Filterregel offengelegt → Anreiz, Häufigkeiten niedriger anzugeben | mittel | Instruktionsregel nur zu Anonymität und Neutralität | ja (2.4) |
| 5 | C | Technologiebeschreibung | „Ergebnisse werden … geprüft“: Indikativ setzt Praxis voraus, nur Nutzen genannt | gering | „neutral, nicht wertend“ nicht operationalisiert | ja (2.4: Modalverben, keine Praxis, keine Vorteile) |
| 6 | C | Instruktion vs. Block TC | Option „kann ich nicht beurteilen“ für alle Aussagen angekündigt, fehlt in TC | gering | keine Regel | ja (2.4) |
| 7 | C | TTF, BI, PERF | Nur gleich gepolte Items; Original so validiert → beibehalten | gering | keine Regel zu gleich gepolten Skalen | ja (2.2, Polung) |
| 8 | A | Konstruktnamen ATAI | Umbenennung in „Vertrauen und Nutzenerwartung“ / „Angst und negative Folgeerwartungen“; UTAUT-naher Begriff | gering | Regel „Konstruktname = Iteminhalt“ lädt zur Umbenennung ein | ja (Regel 6) |
| 9 | D | Tab. D „Validierter Umfang: erfüllt“ | Widerspricht Tab. B („Abweichung“) und Tab. C | gering | Status ohne Kategorie „Abweichung“ und ohne Nachweispflicht | ja (Status mit Nachweis) |
| 10 | D | Tab. B, Einleitung | „32 Items“ statt 35 | gering | keine Zählregel | ja (Zählen der Tabellenzeilen) |
| 11 | D | Literatur P2 | Autorenliste unvollständig (5 Autor:innen laut P2, S. 961) | gering | kein Verbot von Vorwissen bei bibliografischen Angaben | ja (Regel 2; Bibliografie wörtlich in 1a) |
| 12 | D | Literatur S1b | Heftnummer „(2)“ nicht in der Quelle | gering | wie Nr. 11 | ja (wie Nr. 11) |

## 4. Abgeleitete Prompt-Regeln (Priorität)

1. **Geltungsbereich:** Ausschlüsse und Kürzungen nur für das Konstrukt und den Zweck übernehmen, für den die Quelle sie getroffen hat; bei Technologiewechsel den vollständigen Aufgabenkatalog erheben. (Nr. 1, 2)
2. **Belegzitat vor Entscheidung:** jede Auswahl-, Ausschluss- und Skalenentscheidung mit wörtlichem Zitat, das das betroffene Konstrukt nennt; sonst [eigene Bewertung]. (Nr. 2, 3)
3. **Erst extrahieren, dann konstruieren:** Inventar mit wörtlichen Angaben inkl. „betroffenes Konstrukt“ bei Ausschlüssen; Fragebogen nur aus dem Inventar. (Nr. 1, 2, 11, 12)
4. **Kein Vorwissen:** bibliografische Angaben, Seiten und Kennwerte nur aus dem Dokument; Lücken als „nicht in den Quellen enthalten“. (Nr. 11, 12)
5. **Instruktion:** keine Filterregeln oder Hypothesen; Technologiebeschreibung mit Modalverben, ohne Praxis und Vorteile; Optionshinweise blockgenau. (Nr. 4–6)
6. **Konsistenz:** Itemzahlen zählen; Tabelle D nur mit Nachweis, Abweichungen als „Abweichung dokumentiert“. (Nr. 9, 10)

## 5. Nächster Schritt

V6 deckt alle 12 Befunde auf Regelebene ab [eigene Bewertung]. Bei Nr. 1 und 2 ist die Wirkung aber unsicher, weil der Fehler aus dem Verstehen der Quelle entstand. Bei Nr. 10–12 bleibt Zählen und Ergänzen aus Vorwissen eine bekannte Schwäche von Sprachmodellen. Daher: neuen Lauf mit V6 und demselben Fall durchführen, in einer neuen Sitzung gegen dieselben Kriterien (0, A–D) begutachten und die Befundzahlen mit diesem Lauf vergleichen. Wo möglich, Itemwortlaut, Itemzahl und Seitenangaben zusätzlich per Skript gegen Katalog und PDF-Text prüfen.
