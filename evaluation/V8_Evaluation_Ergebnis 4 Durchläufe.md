# Evaluation – Prompt V8 / V8.1 / V8.2: Prüfschleife „Quelleninventar und Fragebogen KI-Readiness (Microsoft Copilot)“

Oct 20, 2026 · @Marianna · Evaluation der Prüfdurchläufe 1–3 und des Kontrolllaufs

## 0. Kurzfazit

1. **Die Belegtreue hat sich deutlich verbessert.** Schwere Befunde (Regelverstöße mit Wirkung auf die Messung) sinken von 4 (Durchlauf 1) über 2 und 0 auf 2 im Kontrolllauf. Theorievermischung, erfundene Zitate, falsche Dateizählung und Ausschluss-Übertragungen kommen ab Durchlauf 3 nicht mehr vor.
2. **Die Befundzahl sinkt aber nicht stetig** (28 → 31 → 18 → 22). Der Grund ist nicht, dass die Korrekturen neue Fehler erzeugen. Der Grund ist, dass jeder Prüflauf nur einen Teil der vorhandenen Mängel findet. Von den 22 Befunden des Kontrolllaufs standen nachweislich mindestens 8 schon in der Fassung nach Durchlauf 1 (Textabgleich, Abschnitt 7.3). Drei Prüfläufe haben sie übersehen.
3. **Hauptursache ist eine fehlende Analogieprüfung.** Ein Befundmuster wird an einer Stelle korrigiert, aber nicht an allen gleichartigen Stellen. Die übrigen Stellen tauchen erst in späteren Läufen auf (z. B. „eindeutig“ in Durchlauf 3, „klar“ im Kontrolllauf; Stichprobenaussage bei S2 und S1, später bei P3).
4. **Die Regeln sind streng genug, aber auf Kosten der Abdeckung.** Die Ergebnisdatei misst nur 4 von 7 Readiness-Dimensionen, Tabelle C ist leer, und die Antwortformate sind uneinheitlich. Das widerspricht den README-Zielen 4 und 8 (Abschnitt 9).
5. **Status der Ergebnisdatei:** korrigiert, aber **nicht freigegeben**. Ein weiterer Kontrolllauf in einem neuen Chat mit 0 Befunden fehlt.

## 1. Metadaten

| Feld | Angabe |
| --- | --- |
| Evaluierter Gegenstand | Prüfschleife des Master-Prompts V8 (Erstellung) und V8.2 (Prüfung) am Fall „Microsoft Copilot“ |
| Fall-Parameter | Microsoft Copilot · Beschäftigte ohne KI-Fachausbildung · vor der Einführung · KI-Readiness · Fragebogensprache Deutsch · Einsatzfelder: Texte entwerfen, zusammenfassen, Daten auswerten, Abläufe planen |
| Quellen | D1 (Itemkatalog), S1a/S1b (MAILS), S2 (ATAI), P1–P5; 9 Dateien |
| Prüfläufe | Durchlauf 1 (28 Befunde), Durchlauf 2 (31), Durchlauf 3 (18), Kontrolllauf nach Durchlauf 3 (22; dieser Chat) |
| Fassungen | Durchlauf1_korrigiert.md, Durchlauf2_korrigiert.md, Durchlauf3_korrigiert.md, Kontrolllauf_korrigiert.md (Ergebnisdatei dieses Chats) |
| Prüfmodell | claude-opus-5-5 (konfiguriert; das ausführende Modell kann abweichen) |
| Bewertungsmaßstab der Evaluation | Prüftabelle V8.2 (I-1 bis II-14); zusätzlich Fehlertypen A–G und Schweregrade (Abschnitt 3) [eigene Bewertung] |
| Vollständigkeit der Eingaben | Fehlerliste 1: Protokollzeile im eingefügten Text leer. Fehlerliste 3: Befund Nr. 18 abgeschnitten (Spalten „korrekte Angabe“ und „Fundstelle“ fehlen); Protokoll nicht eingefügt. Fehlerlisten 1 und 2 wurden je zweimal identisch eingefügt. |

## 2. Untersuchte Prompt-Versionen

| Version | Fundort | Titelzeile im Dokument | Rolle | Verweis im Text |
| --- | --- | --- | --- | --- |
| V8 | Projektdokument „V8 Prompt“ (17.10.2026) | „Prompt V8 – Erstellungsprompt“ | Erstellung (Teil I + II) | „Prüfung … mit dem Prüfprompt V8.2“ |
| V8.1 | Repo `design-entwicklung/V8_1_Erstellung_Fragebogen_master-prompt.md.md` | „Prompt V8 – Erstellungsprompt“ | Erstellung | wie V8 |
| V8.2 | Projektdokument „claude/Prompt V8.2 – Prüfprompt“ (19.10.2026) | „Prompt V8.2 – Prüfprompt“ | Prüfung und Korrektur | „prüft das Ergebnis des Erstellungsprompts V8“; Input 2: „Erstellungsprompt V8“ |
| V8.2 (Repo) | Repo `design-entwicklung/V8_2_Prüfung_Fragebogen_master-prompt.md` | „Prompt V8.2 – Prüfprompt“ | Prüfung | „Erstellungsprompts V8.2“; Input 2: „Erstellungsprompt V8.2“ |

**Abgleich V8 ↔ V8.1:** Gleiche Gliederung (20 Überschriften) und gleiche Liste „Typische Fehler“ (30 Einträge). 14 geprüfte Kernsätze sind wörtlich enthalten (u. a. Rangfolge bei Regelkonflikten, Kopie-Regel, Regel 10, Verstärker-Ausnahme, Selbstkontrolle). Ergebnis: Die Inhalte sind nach Stichprobenabgleich identisch. V8.1 ist nur eine andere Dateibezeichnung von V8 [eigene Bewertung].

**Abgleich V8.2 Projekt ↔ Repo:** Unterschiede nur in Zeile 3 und Input 2 (Versionsverweis). Grundlage dieser Evaluation ist die Projektfassung, die in allen Läufen verwendet wurde.

**Befunde zur Versionsführung**

| Nr. | Befund | Folge | Korrektur |
| --- | --- | --- | --- |
| V-1 | Die Datei heißt „V8_1“, der Titel lautet „Prompt V8“. | Unklar, welche Version ein Lauf verwendet hat. | Titel auf „Prompt V8.1 – Erstellungsprompt“ setzen oder Datei in „V8“ umbenennen; doppelte Endung `.md.md` entfernen. |
| V-2 | Der Repo-Prüfprompt V8.2 verweist auf einen „Erstellungsprompt V8.2“, den es nicht gibt. | Ein Prüflauf mit der Repo-Fassung hat keinen eindeutigen Maßstab. | Verweis auf „Erstellungsprompt V8.1“ (bzw. V8) setzen; Projekt- und Repo-Fassung angleichen. |
| V-3 | `evaluation/evaluation_V7.1.md` enthält keine Evaluation, sondern eine ältere Fassung des Prüfprompts V8.2 (Verweis „Erstellungsprompt V7.2“). | Falsche Einordnung im Ordner `evaluation/`. | Nach `design-entwicklung/` verschieben und als Archivfassung benennen. |
| V-4 | Die Fehlerlisten liegen nur als eingefügter Chattext vor; zwei sind abgeschnitten. | Tabelle D und das Protokoll waren in Durchlauf 3 nicht vollständig belegbar. | Jede Fehlerliste als Datei im Repo ablegen (`evaluation/V8_Fehlerliste_Dn.md`). |

## 3. Vorgehen (Schritt für Schritt)

1. **Inventar der Artefakte:** Prompt-Versionen, vier Fassungen und vier Fehlerlisten erfasst; Dubletten und Lücken festgestellt (Abschnitt 1).
2. **Versionsabgleich:** V8 ↔ V8.1 ↔ V8.2 per Textsuche verglichen (Abschnitt 2).
3. **Normalisierung der Fehlerlisten:** alle Befunde in das Format des Prüfprompts gebracht (Anhänge A–D) und gezählt (Teil I / Teil II).
4. **Klassifikation** je Befund [eigene Bewertung]:
   - **Fehlertyp:** A Fundstelle/Seite/Zitatgenauigkeit · B Bibliografie/Literatur · C fehlender oder unvollständiger Datensatz im Inventar · D nicht markierte Fassungsabweichung (⚠) · E fehlende Dokumentation oder Begründung in Teil II (Belegzitat, Kennwert, Wahl, Pretest-Prüfpunkt) · F inhaltlicher Regelverstoß mit Wirkung auf die Messung (Theorie, Hypothese, erfundenes Zitat, Neutralität, Geltungsbereich) · G Format, Konsistenz, nicht übertragene Folgeänderung.
   - **Schweregrad:** schwer = F · mittel = C, D · gering = A, B, E, G.
5. **Auswertung** je Durchlauf, Fehlertyp und Prüfpunkt (Abschnitte 4–6).
6. **Verlaufsanalyse:** Rückverfolgung der Kontrolllauf-Befunde in die Fassung nach Durchlauf 1 (Textsuche), Musterlücken und Folgefehler (Abschnitt 7).
7. **Ursachenanalyse und Regelvorschläge** für V8.3 (Abschnitt 8); Zielerreichung nach README (Abschnitt 9); Stand der Ergebnisdatei (Abschnitt 10).

## 4. Ergebnis auf einen Blick

| Kennzahl | Durchlauf 1 | Durchlauf 2 | Durchlauf 3 | Kontrolllauf |
| --- | --- | --- | --- | --- |
| Befunde Teil I | 14 | 16 | 10 | 11 |
| Befunde Teil II | 14 | 15 | 8 | 11 |
| **Befunde gesamt** | **28** | **31** | **18** | **22** |
| davon schwer (F) | 4 | 2 | 0 | 2 |
| davon mittel (C, D) | 8 | 9 | 9 | 8 |
| davon gering (A, B, E, G) | 16 | 20 | 9 | 12 |
| fehlende Datensätze | 5 (Nr. 7, 8, 9, 10, 14) [eigene Zählung; Protokoll leer] | 7 (Nr. 7, 8, 9, 13, 14, 15, 16) | 3 (Nr. 2, 3, 4) [eigene Zählung] | 5 (Nr. 4, 5, 6, 10, 11) |
| geprüfte Zeilen Teil I / II | nicht angegeben | 319 / 156 | nicht angegeben | 306 / 142 |
| Befunde je 100 geprüfte Zeilen | – | 6,5 | – | 4,9 |
| Tabelle D ausgegeben | nein | nein | ja | ja (nach Korrektur) |

## 5. Befunde nach Fehlertyp

| Fehlertyp | D1 | D2 | D3 | KL | Summe | Trend |
| --- | --- | --- | --- | --- | --- | --- |
| A Fundstelle/Seite/Zitat | 4 | 6 | 1 | 1 | 12 | ↓ |
| B Bibliografie/Literatur | 8 | 1 | 0 | 3 | 12 | ↓ (Rest Grenzfälle) |
| C fehlender Datensatz | 7 | 7 | 3 | 5 | 22 | konstant |
| D ⚠ nicht markiert | 1 | 2 | 6 | 3 | 12 | ↑ in D3, dann ↓ |
| E Dokumentation Teil II | 2 | 10 | 7 | 6 | 25 | ↑ in D2/D3 |
| F inhaltlicher Regelverstoß (schwer) | 4 | 2 | 0 | 2 | 8 | ↓ |
| G Format/Konsistenz/Folgeänderung | 2 | 3 | 1 | 2 | 8 | konstant niedrig |
| **Summe** | 28 | 31 | 18 | 22 | 99 | |

**Lesart:**
- **F (schwer)** sinkt deutlich. Die Regeln 4, 5, 10 und 11 sowie das Verbot erfundener Zitate wirken ab Durchlauf 2. Die zwei F-Befunde im Kontrolllauf (KL 12, 13) sind keine neuen Fehler, sondern übersehene Altbefunde (Abschnitt 7.3).
- **B (Bibliografie)** wurde in Durchlauf 1 fast vollständig behoben (Literaturverzeichnis). Was bleibt, sind Grenzfälle der Regel „nur Titelseite, Kopf- oder Fußzeile“ (D2 1, KL 1, 2, 21).
- **C (fehlende Datensätze)** tritt in jedem Lauf auf. Das ist das stabilste Fehlermuster: Die Abschnitte „Limitations“ und „Discussion“ werden nicht systematisch durchsucht.
- **D** steigt in Durchlauf 3 an, **E** ist ab Durchlauf 2 der häufigste Typ (25 von 99 Befunden). Das ist die Kehrseite der strengeren DE/EN-Prüfung: Jede neu markierte Abweichung zieht Dokumentationspflichten in Teil II nach sich.

## 6. Befunde nach Prüfpunkt (Mehrfachzuordnung möglich)

| Prüfpunkt | D1 | D2 | D3 | KL | Summe |
| --- | --- | --- | --- | --- | --- |
| I-1 | 3 | 6 | 1 | 1 | 11 |
| I-2 | 1 | 1 | 0 | 2 | 4 |
| I-3 | 1 | 0 | 0 | 0 | 1 |
| I-4 | 0 | 0 | 0 | 0 | 0 |
| I-5 | 1 | 0 | 0 | 0 | 1 |
| I-6 | 0 | 0 | 0 | 0 | 0 |
| I-7 | 5 | 1 | 1 | 0 | 7 |
| I-8 | 2 | 5 | 2 | 5 | 14 |
| I-9 | 0 | 1 | 0 | 0 | 1 |
| I-10 | 1 | 3 | 7 | 3 | 14 |
| II-1 | 1 | 0 | 0 | 1 | 2 |
| II-2 | 2 | 6 | 0 | 1 | 9 |
| II-3 | 1 | 2 | 0 | 0 | 3 |
| II-4 | 0 | 1 | 0 | 0 | 1 |
| II-5 | 0 | 0 | 0 | 1 | 1 |
| II-6 | 0 | 0 | 0 | 0 | 0 |
| II-7 | 0 | 1 | 7 | 3 | 11 |
| II-8 | 0 | 4 | 1 | 2 | 7 |
| II-9 | 0 | 0 | 1 | 1 | 2 |
| II-10 | 0 | 0 | 0 | 0 | 0 |
| II-11 | 2 | 0 | 0 | 0 | 2 |
| II-12 | 0 | 1 | 0 | 1 | 2 |
| II-13 | 2 | 4 | 1 | 2 | 9 |
| II-14 | 7 | 0 | 0 | 1 | 8 |

**Schwerpunkte:** I-8 (Validierungsaussagen, Kennwerte; 14) und I-10 (⚠-Abweichungen; 14) in Teil I; II-7 (Verstärker, Parallelfassungen, Modus; 11), II-2 (Belegzitate; 9) und II-13 (Konsistenz; 9) in Teil II. Nie beanstandet wurden I-4, I-6, II-6 und II-10. Die Auswahllogik (1b), die Itemvollständigkeit, die Filter- und Aggregationslogik sowie die Skalenregeln waren also ab dem ersten Lauf stabil.

## 7. Verbesserungslinie

### 7.1 Was sich nachweislich verbessert hat

| Bereich | Stand Durchlauf 1 | Stand Ergebnisdatei | Beleg |
| --- | --- | --- | --- |
| Theorietrennung bei Hypothesen | H1 (TTF → PERF) trotz unbelegter TTF-Herkunft übernommen | Tabelle C leer; H1, H2 und S2-Hypothese mit Herkunft beider Konstrukte unter „Offene Punkte“ | D1 15, 16, 22 |
| Erfundene Zitate | „als Skala nicht validiert“ als Quellzitat (S. 323) ausgegeben | Einzelindikator-Beleg wörtlich (S. 323) | D1 17 |
| Dateizählung, Kopie-Regel | „Original und Kopie“ angenommen | 9 Dateien; Kopie ist Quelle | D1 1 |
| Literaturverzeichnis | 6 Einträge ohne Kennzeichnung fehlender Angaben | alle Lücken als „nicht in den Quellen enthalten“; Heft bei Carolus korrigiert | D1 23–28; KL 21 |
| Geltungsbereich (Regel 4) | Ladungskennwert auch für entferntes Item TC_Performance_3 | Ausnahme für TC_Performance_3 ausgewiesen | D2 22 |
| Format Tabelle B | zusammengefasste Zellen, fehlende Spalten | eine Zeile je Item, 8 Spalten, 59 Zeilen gezählt | D2 17 |
| DE/EN-Abweichungen | 0 ⚠ zu „meine Aufgaben“, Modus, „eindeutig“ | ⚠ Nr. 1–24, jede mit Wahl, Begründung und Pretest-Prüfpunkt in Teil II | D1 12; D2 11, 12; D3 4–10; KL 7–9 |
| Neutralität der Technologiebeschreibung | Begriff „künstliche Intelligenz“ (kommt in den ATAI-Items vor) | gestrichen | KL 12 |
| Validierungsaussagen in C4 | Stichprobe, Stimulus, externe Validierung fehlten | je Quelle ergänzt (S1b S. 8; S2 S. 116; P3 S. 320, 323, 325, 326) | D2 9, 14; D3 2, 3; KL 4–6, 10, 11 |

### 7.2 Musterlücken: dasselbe Muster, in mehreren Läufen stückweise gefunden

| Muster | zuerst gefunden | später an anderer Stelle | Läufe bis vollständig |
| --- | --- | --- | --- |
| Bibliografie aus unzulässiger Stelle | D2 1 (P1, „Please cite as“) | KL 1, 2, 21 (S1a, S1b) | 2 |
| Stichprobeneinschränkung als Validierungsaussage | D2 9 (S2) | D3 2 (S1); KL 11 (P3) | 3 |
| „eindeutig“ nur in der DE-Fassung | D3 5–9 (Items) | KL 7 (Aufgabenbeschreibung) | 2 |
| Verstärker ohne Kennwert/Beleg | D3 12–17 („eindeutig“) | KL 17, 18 („klar“) | 2 |
| DE/EN-Abweichung in Instruktions-/Blocktexten | D2 20, 21 (Creativity, PERF) | D3 4 (TTF-Instruktion); KL 8 (Blockfrage Execution) | 3 |
| Seitenangaben ungenau | D1 3–5 | D2 2–6; D3 1; KL 3 | 4 |
| fehlende Datensätze in C4 | D1 7–11, 14 | D2 7–9, 13–16; D3 2–4; KL 4–6, 10, 11 | 4 (nicht abgeschlossen) |

**Folgerung:** 14 der 22 Kontrolllauf-Befunde (KL 1, 2, 7, 8, 9, 11, 15, 16, 17, 18, 20, 21 sowie die Ableitungen 13, 14) wären durch eine konsequente Analogieprüfung in früheren Läufen gefunden worden [eigene Bewertung].

### 7.3 Übersehene Altbefunde (Recall des Prüfprompts)

Textsuche in der Fassung nach Durchlauf 1: Diese Mängel aus dem Kontrolllauf waren schon dort enthalten und wurden in den Durchläufen 2 und 3 nicht beanstandet.

| KL-Nr. | Mangel | in Fassung D1 vorhanden |
| --- | --- | --- |
| 1 | S1a-Bibliografie aus Literaturangabe „(PDF-S. 3)“ | ja |
| 2 | S1b-Autor:innen als Initialen | ja |
| 3 | P4 „decision-makers“ (S. 1) | ja |
| 7 | TC-Intellective-Beschreibung ohne ⚠ | ja |
| 12 | „… das auf künstlicher Intelligenz beruht“ in Block 2 | ja |
| 13 | ATAI05-Beleg („more employed people“) nicht im Inventar | ja |
| 19 | Polung Block 6 ohne Kennwert | ja |
| 21 | Carolus „1(2)“ im Literaturverzeichnis | ja |

**Folgerung:** Eine sinkende Befundzahl ist kein ausreichender Qualitätsnachweis. Eine Freigabe braucht entweder einen Lauf mit 0 Befunden oder eine skriptgestützte Teilprüfung (Abschnitt 11).

### 7.4 Nicht übertragene Folgeänderungen (Teil I → Teil II)

| Teil-I-Befund | nicht übertragen nach Teil II | aufgedeckt in |
| --- | --- | --- |
| D1 12 (⚠ „meine Aufgaben“) | 20 TTF-Items ohne Wahl/Pretest | D2 18 |
| ⚠ Nr. 9, 15 (D1-Fassung) | Block 1 (Creativity), Block 5 (PERF) | D2 20, 21 |
| D3 4–9 | Block 3, Items mit „eindeutig“ | D3 11–17 |
| D3 3 (Stimulus) | Tabelle A, Offene Punkte | D3 18 |
| KL 11 (Stichprobe P3) | Tabelle A, Offene Punkte | KL 20 (im selben Lauf) |

Der Prüfprompt verlangt zwar „alle Folgeänderungen nachziehen“, gibt aber keine Zuordnung vor, an welcher Stelle in Teil II ein Inventareintrag wirken muss.

## 8. Ursachenanalyse und Regelvorschläge für V8.3

Spalte „Abdeckung in V8/V8.2“: ja = Regel vorhanden, Fehler ist ein Anwendungsfehler · teilweise = Regel vorhanden, Begriff oder Umfang aber unbestimmt · nein = keine Regel [eigene Bewertung].

| Nr. | Problem | Belege (Befund-Nr.) | Ursache im Prompt | Abdeckung V8/V8.2 | Vorschlag (Regeltext für V8.3) |
| --- | --- | --- | --- | --- | --- |
| U-1 | Muster nur stückweise gefunden | Abschnitt 7.2 | Prüfprompt prüft Zeile für Zeile, ohne Musterübertragung | nein | **Prüfprompt, Vorgehen Nr. 6:** „Prüfe für jeden Befund, ob dasselbe Muster an anderen Stellen vorkommt (andere Quelle, anderer Block, Items, Aufgabenbeschreibungen, Instruktionen, Blockfragen). Liste jede Fundstelle als eigenen Befund im selben Durchlauf.“ |
| U-2 | Befundmuster früherer Läufe werden nicht auf den ganzen Entwurf angewendet | Abschnitt 7.3 | Fehlerlisten früherer Durchläufe dienen nur für Tabelle D | nein | **Prüfprompt, Vorgehen Nr. 7:** „Wende jedes Befundmuster aus den eingefügten Fehlerlisten auf den gesamten Entwurf an, bevor du neue Befunde suchst.“ |
| U-3 | fehlende Validierungsaussagen in C4 | D1 7, 11; D2 9, 14, 15; D3 2, 3; KL 4–6, 10, 11 | „Validierungsaussagen nicht übersehen“ ohne Suchraum | teilweise | **Erstellung 1c C4:** „Durchsuche die Abschnitte Methods, Results, Discussion und Limitations jeder ausgewählten Quelle. Nimm jede Aussage zu Stichprobe, Stimulus, Faktorstruktur, externer Validierung, Itemkonstruktion, Invarianz und formativen Kennwerten (VIF, Gewichte) mit Bezug auf.“ |
| U-4 | DE/EN-Abweichungen in Texten außerhalb der Items übersehen | D2 20, 21; D3 4; KL 7, 8 | Schwelle für „Abweichung“ und Geltungsbereich unbestimmt | teilweise | **Erstellung 1c:** „Markiere jede DE/EN-Abweichung, bei der eine Fassung ein Wort enthält, das in der anderen fehlt und die Aussage verstärkt, einschränkt oder den Kontext ändert – in Items, Aufgabenbeschreibungen, Instruktionen und Blockfragen.“ |
| U-5 | Verstärker nicht erkannt | D3 12–17; KL 17, 18 | Begriff „Verstärker“ nicht definiert | teilweise | **Erstellung 2.2:** „Verstärker sind Wörter, die Ausmaß oder Gewissheit steigern (z. B. ‚eindeutig‘, ‚klar‘, ‚strikt‘, ‚immer‘, ‚sehr‘, ‚vollständig‘, ‚tatsächlich‘, ‚direkt‘). Prüfe jedes Item gegen diese Liste.“ |
| U-6 | Bibliografie aus Literaturangaben im Fließtext | D2 1; KL 1, 2, 21 | Itemblätter ohne Titelseite nicht geregelt | teilweise | **Erstellung Regel 2:** „Bei Dokumenten ohne Titelseite (z. B. Itemblatt) nur Kopf- oder Fußzeile verwenden; die übrigen Angaben aus dem zugehörigen Paper. ‚Please cite as‘-Blöcke und Referenzzeilen am Dokumentende sind keine zulässige Fundstelle.“ |
| U-7 | geschätzte Seitenzahl | D1 3–5; D2 2–6; D3 1; KL 3 | Seiten ohne gedruckte Zahl nicht ausdrücklich geregelt | teilweise | **Erstellung Regel 1:** „Trägt eine Seite keine gedruckte Seitenzahl (Deckblatt, erste Artikelseite), gib ‚PDF-S. n‘ an. Gib eine Seite nie aus einem Seitenbereich ab.“ |
| U-8 | Zitate in Teil II ohne Inventarzeile | D1 17; KL 13 | Regel vorhanden, aber nicht prüfbar verknüpft | ja | **Erstellung Schritt 2:** „Jedes Zitat in Teil II nennt seine Inventarzeile (z. B. ‚Inv. C4-S2-5‘). Fehlt sie, nimm das Zitat zuerst in Teil I auf.“ |
| U-9 | Teil-I-Einträge wirken nicht in Teil II | Abschnitt 7.4 | keine Übertragungsliste | nein | **Erstellung, Ausgabe Teil II Nr. 8 (neu):** „Übertragungsliste: jede ⚠-Nr. und jede Validierungsaussage aus C4 → Stelle in Teil II (Tabelle A/B, Offene Punkte) oder ‚nicht relevant‘ mit Grund.“ |
| U-10 | Begriffe aus allgemeinen Instrumenten in der Technologiebeschreibung | KL 12 | Regel nennt als Beispiel nur Aufgabenarten | ja | **Erstellung 2.4:** „Prüfe die Technologiebeschreibung gegen den Wortlaut aller Blöcke, auch allgemeiner Instrumente (z. B. ‚künstliche Intelligenz‘ bei ATAI).“ |
| U-11 | wiederholte Standardtexte in Tabelle B (z. B. 20 × gleicher ⚠-Hinweis) | D2 17 → D3 11–17 | „keine zusammengefassten Zellen“ zwingt zu Wiederholungen; Fehlerfläche wächst | nein | **Erstellung, Formatregeln:** „Wiederkehrende Adaptionshinweise eines Blocks einmal als Blockhinweis mit Kennung (z. B. B3-a) formulieren; in der Itemzeile nur die Kennung nennen.“ |
| U-12 | Protokoll und Zeilenzählung fehlen in einzelnen Läufen | D1, D3 ohne gezählte Zeilen | Pflicht steht im Ausgabeformat, wird aber übersprungen | ja | **Prüfprompt, Ausgabe:** „Ohne Protokollzeile ist die Fehlerliste unvollständig.“ |
| U-13 | Schweregrad nicht erfasst | alle Läufe | Fehlerliste ohne Gewichtung | nein | **Prüfprompt, Fehlerliste:** zusätzliche Spalte „Schwere (schwer/mittel/gering)“ mit Definition wie Abschnitt 3. |
| U-14 | kein Freigabekriterium nach Durchlauf 3 | dieser Kontrolllauf | „Im Durchlauf 3 … entfernen“ beendet die Schleife ohne Prüfung der Korrektur | nein | **Prüfprompt, Schritt 2:** „Nach Durchlauf 3 folgt ein Kontrolllauf in neuem Chat. Freigabe nur bei 0 schweren und 0 mittleren Befunden; geringe Befunde gehen in ‚Offene Punkte‘.“ |

## 9. Zielerreichung der Ergebnisdatei (README-Ziele) [eigene Bewertung]

| Ziel (README) | Stand Ergebnisdatei | Bewertung | Beleg |
| --- | --- | --- | --- |
| 1 Theoriebasierung | Theorie je Konstrukt laut Herkunftsangabe; TTF-Herkunft nicht in den Quellen enthalten | teilweise | Tabelle A, Dim. 3 |
| 2 Theoretische Herleitung | jedes Item mit Konstrukt, Fundstelle, Herkunft | erfüllt | Tabelle B (59 Zeilen) |
| 3 Theorietrennung | ein Konstrukt = eine Quelle; keine theorieübergreifende Hypothese | erfüllt | Tabelle C leer; Offene Punkte Nr. 8 |
| 4 Hypothesenableitung | keine Hypothese aufgenommen | nicht erfüllt (Zielkonflikt mit Regel 11) | Offene Punkte Nr. 8 |
| 5 Quellenbindung | alle Angaben mit Fundstelle; Eigenes als [Modellwissen]/[eigene Bewertung] | erfüllt | Tabelle D |
| 6 Eindimensionalität | Begriffspaare aus validierten Originalen beibehalten, mit Kennwert/Beleg | teilweise (bewusst) | Tabelle B, z. B. TC_Judgmental_2 |
| 7 Neutralität | Beschreibung bereinigt; Verstärker belegt, Pretest-Prüfpunkte | weitgehend erfüllt | Block 2; KL 12, 17, 18 |
| 8 Einheitliches Antwortformat | drei Formate (F6, L5, L11) | nicht erfüllt (Zielkonflikt mit Regel 10) | Antwortformate |
| 9 Transparenz | Zuordnung Dimension → Theorie → Konstrukt → Item → Quelle | erfüllt | Tabellen A, B |
| 10 Praxistauglichkeit | 59 Items, Filterlogik, drei Skalen; nur mit Online-Tool umsetzbar | teilweise | Blöcke 1–6 |
| 11 Reproduzierbarkeit | 4 Läufe, Befundzahlen schwanken (28/31/18/22) | teilweise | Abschnitt 4 |
| Abdeckung der Readiness-Dimensionen | 4 von 7 gemessen (2, 3, 4, 5); 1, 6, 7 offen | teilweise | Offene Punkte Nr. 1, 2 |

**Zielkonflikt:** Die Regeln 10 (validierte Skalen unverändert) und 11 (Hypothesen nur innerhalb einer Theorie) sichern die Validität. Sie verhindern aber die Ziele 4 und 8 und die Messung der Dimension KI-Kompetenz. Das ist kein Prompt-Fehler, sondern eine Entscheidung, die offen festgehalten werden sollte. Vorschlag: README-Ziel 8 auf „Originalformat je Instrument“ umformulieren und Ziel 4 auf „nur theorieintern belegte Hypothesen“ begrenzen.

## 10. Ergebnisdatei aus diesem Chat

| Feld | Angabe |
| --- | --- |
| Datei | Quelleninventar_und_Fragebogen_KI-Readiness_Copilot_Kontrolllauf_korrigiert.md |
| Grundlage | Fassung nach Durchlauf 3 + 22 Befunde des Kontrolllaufs |
| Umfang | Teil I (9 Quellen, Vollinventar S1, S2, P3; 24 ⚠-Markierungen); Teil II (Instruktion, Tabelle A mit 7 Dimensionen, Tabelle B mit 59 Items in Blöcken 1, 3–6, Block 2 Technologiebeschreibung, Tabelle C leer, Auswertung, 12 Offene Punkte, 7 Literatureinträge); Tabelle D (14 + 10 Prüfpunkte); Abschluss |
| Gemessene Instrumente | TC (Filter, 24), TTF (24), BI (3), PERF (3) aus P3/D1 Q3; ATAI Acceptance/Fear (5) aus S2 |
| Entfernt nach Regel 9 | nichts |
| Status | korrigiert, **nicht freigegeben** (kein Lauf mit 0 Befunden) |

**Eingearbeitete Änderungen des Kontrolllaufs**

| KL-Nr. | Stelle in der Ergebnisdatei | Änderung |
| --- | --- | --- |
| 1 | 1a, S1a | Bibliografie nur aus Kopfzeile; Verweis auf S1b; Heft nicht enthalten |
| 2 | 1a, S1b | Autor:innen wörtlich; Heft nicht enthalten |
| 3 | 1a, P4 | „PDF-S. 2“ (3 Zitate) |
| 4 | C4 S1 | Validierungsaussage externe Validierung (S1b, S. 8) |
| 5 | C4 S2, Ausschlüsse | Aussage zu Item 05 bei beschäftigten Stichproben (S. 116) |
| 6 | C4 S2 | Validierungsaussage Itemkonstruktion (S. 116) |
| 7 | C3 P3, TC Intellective | ⚠ Abweichung „eindeutig“ |
| 8 | C3 P3, TTF Execution | ⚠ Abweichung „klar definierter“ |
| 9 | ⚠-Liste | Nr. 23, 24 |
| 10 | C4 P3 | VIF und Gewichte TC/TeC (S. 323) |
| 11 | C4 P3 | Stichprobe Clickworker (S. 326) |
| 12 | Block 2 | „das auf künstlicher Intelligenz beruht“ gestrichen |
| 13 | Tabelle B, S2-ATAI05 | vollständiges Zitat aus Inventar; Regel 10 |
| 14 | Tabelle A, ATAI Fear | Begründung Item 05 mit Regel 10 und Beleg |
| 15 | Block-Instruktionen Block 1 | ⚠ Nr. 23 dokumentiert |
| 16 | Block-Instruktionen Block 3 | ⚠ Nr. 24 dokumentiert |
| 17 | Tabelle B, TC_Performance_1 | Verstärker „klar“ mit Kennwert |
| 18 | Tabelle B, TTF_Performance_1 | Verstärker „klar“ mit Beleg und Pretest |
| 19 | Polung Block 6 | Ladungen und α |
| 20 | Tabelle A Dim. 3; Offene Punkte Nr. 10 | Stichprobe P3 |
| 21 | Literaturverzeichnis Carolus | Heft nicht enthalten |
| 22 | Tabelle D; Abschluss | neu erstellt; Protokoll D1 = 14/14 |

## 11. Empfehlungen und nächste Schritte (priorisiert)

1. **Kontrolllauf 2** mit der Ergebnisdatei in einem neuen Chat mit Prüfprompt V8.2 und allen vier Fehlerlisten. Ziel: 0 schwere und 0 mittlere Befunde.
2. **Prompt V8.3** mit den Regeln U-1 bis U-14 erstellen (Erstellung: U-3 bis U-11; Prüfung: U-1, U-2, U-12 bis U-14). Danach einen Neulauf am selben Fall durchführen und die Befundzahlen mit Abschnitt 4 vergleichen.
3. **Skriptgestützte Teilprüfung** vor jedem Prüflauf: Zeilen von Tabelle B zählen; Begriffe der Technologiebeschreibung gegen alle Items abgleichen; Verstärkerliste per Textsuche; jedes Zitat gegen den PDF-Text suchen.
4. **Deutsche MAILS-Fassung beschaffen** (Offener Punkt Nr. 1). Damit wird Dimension 1 messbar, ohne Regel 10 zu verletzen.
5. **Versionsführung bereinigen** (V-1 bis V-4) und diese Evaluation als `evaluation/Evaluation_V8.md` ablegen.

## 12. Fazit: Wie Prompt V8 geändert und der Durchlauf geführt werden sollte

### 12.1 Was realistisch erreichbar ist

Ein Sprachmodell liefert auch mit einem besseren Prompt kein garantiert fehlerfreies Ergebnis in einem einzigen Lauf. Die vier Läufe zeigen das: Jeder Prüflauf findet nur einen Teil der vorhandenen Mängel (Abschnitt 7.3). Erreichbar ist ein **freigabefähiges Ergebnis**: 0 schwere und 0 mittlere Befunde in einem unabhängigen Kontrolllauf, geringe Befunde dokumentiert unter „Offene Punkte“. Dafür müssen sich zwei Dinge ändern: der Prompt (12.2) und der Ablauf (12.3).

### 12.2 Änderungen am Master-Prompt (V8 → V8.3)

Die fünf wirksamsten Änderungen, nach erwartetem Effekt geordnet [eigene Bewertung]:

| Rang | Änderung | wo im Prompt | behebt (Befunde) | erwartete Wirkung |
| --- | --- | --- | --- | --- |
| 1 | **Analogieprüfung** im Prüfprompt: jeden Befund an allen gleichartigen Stellen suchen; Befundmuster früherer Läufe zuerst auf den ganzen Entwurf anwenden (U-1, U-2) | Prüfprompt, Vorgehen | Abschnitt 7.2 und 7.3; im Kontrolllauf 14 von 22 | weniger Läufe bis zur Freigabe; kein „Tröpfeln“ von Befunden |
| 2 | **Suchraum-Checkliste für C4** (Methods, Results, Discussion, Limitations; Stichprobe, Stimulus, externe Validierung, Itemkonstruktion, Invarianz, VIF/Gewichte) (U-3) | Erstellung 1c | C-Befunde in jedem Lauf (5/7/3/5) | stabilstes Fehlermuster beseitigt |
| 3 | **Begriffe festlegen:** Verstärkerliste, Schwelle für DE/EN-Abweichungen inkl. Instruktions- und Blocktexten, zulässige Bibliografie-Stellen, „PDF-S.“ bei Seiten ohne Zahl (U-4 bis U-7) | Erstellung Regeln 1, 2; 1c; 2.2 | D-, A-, B-Befunde | Ermessensspielraum des Modells sinkt; Prüfer und Ersteller urteilen gleich |
| 4 | **Verknüpfung Teil I → Teil II:** Inventarzeilen-ID bei jedem Zitat in Teil II; Übertragungsliste für jede ⚠-Nr. und Validierungsaussage (U-8, U-9) | Erstellung Schritt 2; Ausgabe Teil II | Abschnitt 7.4; KL 13, 20 | keine Zitate außerhalb des Inventars; Folgeänderungen prüfbar |
| 5 | **Blockhinweise mit Kennung statt Wiederholung** in Tabelle B (U-11) und **Schweregrad-Spalte** in der Fehlerliste (U-13) | Erstellung Formatregeln; Prüfprompt Ausgabe | E-Befunde (Dokumentation) | kleinere Fehlerfläche; Prüfung konzentriert sich auf schwere Befunde |

Zusätzlich: **Versionsführung bereinigen** (V-1 bis V-4) und den **Zielkonflikt** mit den README-Zielen 4 und 8 ausdrücklich festhalten (Abschnitt 9).

### 12.3 Empfohlener Ablauf eines Durchlaufs

Der wichtigste Unterschied zum bisherigen Ablauf: **Teil I wird vollständig geprüft und eingefroren, bevor Teil II entsteht.** Bisher wurden beide Teile gemeinsam erstellt und geprüft. Dadurch musste jede Inventarkorrektur nachträglich nach Teil II übertragen werden, und genau dort entstanden die Folgefehler (Abschnitt 7.4).

| Schritt | Chat | Was | Ergebnis | Abbruch-/Freigabekriterium |
| --- | --- | --- | --- | --- |
| 0 | – | Versionen festlegen (Erstellung V8.3, Prüfung V8.3), Quellen vollständig hochladen, Fall-Parameter eintragen | Lauf-Steckbrief | Versionsverweise in beiden Prompts stimmen überein |
| 1 | A (neu) | Erstellungsprompt: **nur Teil I** (Inventar) | Inventar-Entwurf | – |
| 2 | – | Skriptprüfung Teil I: Zitate gegen PDF-Text, Seitenangaben, Itemzahlen | Abweichungsliste | technische Fehler vorab korrigiert |
| 3 | B (neu) | Prüfprompt: **nur Teil I**, mit Analogieprüfung; „korrigieren“ | geprüftes Inventar | 0 schwere/mittlere Befunde → Inventar **einfrieren**; sonst Schritt 3 erneut in neuem Chat (max. 3×) |
| 4 | C (neu) | Erstellungsprompt: **nur Teil II** aus dem eingefrorenen Inventar, mit Übertragungsliste | Fragebogen-Entwurf | – |
| 5 | – | Skriptprüfung Teil II: Zeilen in Tabelle B zählen, Begriffe der Technologiebeschreibung gegen alle Items, Verstärkerliste, Blocknummern | Abweichungsliste | technische Fehler vorab korrigiert |
| 6 | D (neu) | Prüfprompt: **Teil II gegen das eingefrorene Inventar**; „korrigieren“ | korrigierter Fragebogen | max. 3 Durchläufe, jeder in neuem Chat |
| 7 | E (neu) | **Kontrolllauf** über Teil I + II mit allen Fehlerlisten | Tabelle D | **Freigabe** nur bei 0 schweren und 0 mittleren Befunden |
| 8 | – | Archivieren: jede Fehlerliste und jede Fassung als Datei im Repo (`evaluation/`, `demonstration/`) | vollständige Dokumentation | keine abgeschnittenen Listen |

**Regeln für jeden Prüfchat:** neuer Chat ohne Erstellungsverlauf; alle früheren Fehlerlisten vollständig als Datei einfügen; Durchlauf-Nr. eintragen; Protokollzeile mit gezählten Zeilen ist Pflicht.

### 12.4 Zusammenfassung der Vorgehensweise beim Master-Prompt

Der Master-Prompt wurde von V1 bis V8 schrittweise aus Evaluationsbefunden weiterentwickelt. Mit V8 steht ein zweistufiges Verfahren: Ein Erstellungsprompt baut aus den Quellen zuerst ein wörtlich belegtes Inventar und daraus den Fragebogen. Ein getrennter Prüfprompt (V8.2) prüft beides in bis zu drei Durchläufen gegen Quellen und Regelwerk.

Die Evaluation der Läufe zu V8 zeigt: Das Regelwerk erfüllt seinen Hauptzweck. Theorievermischung, erfundene Zitate und Vorwissen kommen in der Ergebnisdatei nicht mehr vor, und jede Angabe ist mit Fundstelle belegt. Die verbleibenden Schwächen liegen weniger in fehlenden Regeln als im **Ablauf**: Prüfläufe finden Mängel nur stückweise, Korrekturen am Inventar werden nicht sicher in den Fragebogen übertragen, und unbestimmte Begriffe (Verstärker, Abweichung, zulässige Fundstelle) lassen Ermessensspielraum.

Für V8.3 empfiehlt sich daher: Analogieprüfung im Prüfprompt; feste Begriffsdefinitionen und eine Suchraum-Checkliste im Erstellungsprompt; eine nachprüfbare Verknüpfung von Inventar und Fragebogen; und ein Ablauf, der Teil I vor Teil II freigibt, Skriptprüfungen vorschaltet und mit einem unabhängigen Kontrolllauf endet. Freigegeben wird erst bei 0 schweren und 0 mittleren Befunden. Bewusst bleibt der Zielkonflikt zwischen Validierungstreue und Abdeckung: Lieber eine Dimension als offenen Punkt ausweisen als eine nicht validierte Fassung einsetzen.


---

# Anhänge

Die Fehlerlisten stehen im Format des Prüfprompts V8.2. Die Spalten „Typ“ und „Schwere“ sind Ergänzungen dieser Evaluation [eigene Bewertung].

## Anhang A – Fehlerliste Durchlauf 1

| Nr. | Teil | Abschnitt/Tabelle | Zeile bzw. Item-ID bzw. H | Prüfpunkt | Befund | korrekte Angabe | Fundstelle | Typ | Schwere |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | I | 1a | Dateianzahl, Kopie-Regel | I-3 | Zählung falsch. Für P1–P3 wird „Original und Kopie“ angenommen, im Projekt liegen P1, P2 und P3 aber nur als „- Kopie“ vor. | „Anzahl vorliegender Dateien: 9 (D1 + 8 PDF). P1, P2, P3 liegen nur als Kopie vor; die Kopie ist die Quelle. Eine Prüfung auf Inhaltsgleichheit entfällt.“ Folgeänderung: ⚠ Nr. 1 streichen. | Projektdateiliste | F | schwer |
| 2 | I | ⚠-Liste | Nr. 2 (P2, Autor:innen) | I-2 | Die Reihenfolge ist im Kopfbereich bestätigt (Leserichtung: Wichmann, Behn, Degirmenci, Leyer, Barros). Das ⚠ ist damit unnötig. | Autor:innen wie in 1a, ⚠ entfällt | P2, S. 961 | B | gering |
| 3 | I | 1a | S1b, Spalte Antwortskala | I-1 | Fundstelle „S. 5“ ist falsch, die Skala steht auf S. 6. | „ja (S. 6)“ | S1b, S. 6 | A | gering |
| 4 | I | 1c S1, C3 | Begründung der Skala | I-1 | Fundstelle „S1b S. 5–6“ ist falsch, der Text steht vollständig auf S. 6. | „S1b S. 6“ | S1b, S. 6 | A | gering |
| 5 | I | 1c S1, C2 | MAILS-13 | I-1 | Fundstelle „S1a PDF-S. 1–2“ ist falsch, das Item steht vollständig auf PDF-S. 1. | „S1a PDF-S. 1; S1b S. 9“ | S1a, PDF-S. 1 | A | gering |
| 6 | I | 1c S1, C3 | Instruktion | I-7 | Der Instruktionstext ist unvollständig, der letzte Satz fehlt. | ergänzen: „Please circle the value that best describes your ability.“ | S1a, PDF-S. 1 | C | mittel |
| 7 | I | 1c S1, C4 | Validierungsaussagen | I-8 | Fehlender Datensatz zur Einschränkung der Modellprüfung | „it is necessary to consider our approach exploratory“ (Bezug: Faktorenstruktur MAILS) | S1b, S. 8 | C | mittel |
| 8 | I | 1c S1, C3 | Erhebungssprache / andere Sprachfassungen | I-7 | Fehlender Datensatz zur Übersetzung (relevant für Regel 10 und Offene Punkte Nr. 1) | „Additional effort is necessary to translate the questionnaire and validate it.“ | S1b, S. 8 | C | mittel |
| 9 | I | 1c S2, C3 | Erhebungssprache | I-7 | Fehlender Datensatz zur Entwicklungssprache. Das ⚠ zur Zuordnung Deutschland → Deutsch bleibt bestehen. | ergänzen: „The items of the ATAI scale […] were developed in German language, translated into Chinese and English, and then back translated […]“ | S2, S. 111 | C | mittel |
| 10 | I | 1c S2, C3 | Szenario / Blockreihenfolge | I-7 | Fehlender Datensatz: Ergebnis der Kontrollerhebung zur Einführung vor der ATAI-Skala | „we conclude that the introduction did not bias participants’ response style“ (Kontrollerhebung, N = 82, China) | S2, S. 112 | C | mittel |
| 11 | I | 1c S2, C4 | Invarianz | I-8 | Unvollständig, genannt sind nur „equal loadings“. | ergänzen: „no scalar measurement invariance was found across the samples from the different countries“ | S2, S. 114 | C | mittel |
| 12 | I | 1c P3, C2 | TTF_Planning_2/3, TTF_Creativity_2/3, TTF_Intellective_2/3, TTF_Judgmental_2/3, alle TTF_Conflict, TTF_MixedMotive, TTF_Contest und TTF_Performance (20 Items) | I-10 | ⚠ fehlt: DE lautet „meine Aufgaben“, EN nur „tasks“ (ohne „my“). | „⚠ Abweichung (DE ‚meine Aufgaben‘ / EN ‚tasks‘)“ ergänzen und in die ⚠-Liste aufnehmen | D1 Fragebogen 3, Abschnitt TTF | D | mittel |
| 13 | I | 1c P3, C1 | Immersion, Interactivity, Social presence | I-5 | Der Nachweis der Sekundärzitate im Literaturverzeichnis fehlt. | „Lit.-Verz. S. 328“ (Witmer & Singer; Poeschl & Doering); „Lit.-Verz. S. 327“ (Liu) | P3, S. 327–328 | A | gering |
| 14 | I | 1c P3, C3 | Messverfahren | I-7 | Fehlender Datensatz zu den Aufmerksamkeitsprüfungen | „two attention checks and one control question were included to ensure data quality“ (S. 322); D1: Die Abbildung im Abschnitt „Use Context“ enthält einen Attention Check („number 19“). | P3, S. 322; D1 Fragebogen 3, Abschnitt TeC | C | mittel |
| 15 | II | Tabelle C | H1 | II-11 | Regel 11 verletzt. Die Herkunft der TTF-Items ist nicht in den Quellen enthalten, damit ist die Theoriegleichheit nicht belegt. Die Angabe aus dem Abstract (S. 319) betrifft das Rahmenmodell des Papers, nicht das Konstrukt (Regel 5). | H1 entfernen; Tabelle C: „keine“. Unter „Offene Punkte“: „H1 (TTF → PERF) nicht aufgenommen: Herkunft der TTF-Items nicht in den Quellen enthalten; PERF: Goodhue & Thompson (1995, zit. n. Paetow et al., 2026) (Regel 11)“. Offene Punkte Nr. 9 entfällt. | Inventar C2 P3 (TTF), C5 H1, ⚠ Nr. 18 | F | schwer |
| 16 | II | Tabelle A | Zeile 3 (TTF), Theorie/Instrument | II-3 | Das Rahmenmodell ist als Theorie angegeben, und Goodhue & Thompson wird ohne Herkunftsangabe für TTF zugeordnet. | „TTF-Items aus P3/D1 Q3 (Paetow et al., 2026); Herkunft nicht in den Quellen enthalten“ | Inventar C2 P3 | F | schwer |
| 17 | II | Tabelle A | Zeile 3 (TTF), validiert | II-1 | „als Skala nicht validiert“ ist als Quellzitat mit S. 323 ausgewiesen, der Wortlaut steht aber nicht in P3. | „nein: Einzelindikator; Beleg: ‚TTF was modeled as a participant-specific single-indicator variable‘ (S. 323); als Skala nicht validiert“ | Inventar C4 P3 | F | schwer |
| 18 | II | Tabelle A | Zeile 1 (MAILS), validiert | II-13 | Die α-Spanne „.71–.93“ widerspricht C4 (Persuasion literacy α = .66). | „ja: α .66–.93; AI Ethics wörtlich ‚= 75‘ (S1b S. 6)“ | Inventar C4 S1 | G | gering |
| 19 | II | Tabelle A | Zeile 4 (PERF), Belegzitat | II-2 | Das Zitat nennt weder PERF noch den Arbeitskontext. | „This study investigated how task-technology fit (TTF) relates to perceived performance (PERF) and behavioral intention to use (BI) virtual reality (VR) for work tasks in a pre-adoption context.“ (S. 324). Vorher in das Inventar aufnehmen (C3/C4 P3). | P3, S. 324 | E | gering |
| 20 | II | Tabelle A | Zeile 5 (BI), Belegzitat | II-2 | „wie Zeile 4“ übernimmt denselben Mangel. | Zitat wie Nr. 19 | P3, S. 324 | E | gering |
| 21 | II | Offene Punkte | Nr. 12 | II-13 | Folgefehler aus Nr. 1: Es liegen nur Kopien vor. | Punkt streichen | Projektdateiliste | G | gering |
| 22 | II | Offene Punkte | Nr. 8 (H2) | II-14 / II-11 | Das Sekundärzitat steht nicht im vorgeschriebenen Format, und die TTF-Herkunft ist als „TTF-Modell“ angegeben. | „H2 (TTF → BI): TTF-Herkunft nicht in den Quellen enthalten; BI: UTAUT, Venkatesh et al. (2003, zit. n. Paetow et al., 2026) (Regel 11)“ | Inventar C2 P3 | B | gering |
| 23 | II | Literaturverzeichnis | Do Khac et al. (2025) | II-14 | Fehlende Angaben sind nicht gekennzeichnet. | „Jahrgang, Heft, Seiten: nicht in den Quellen enthalten“ ergänzen | Inventar 1a P4 | B | gering |
| 24 | II | Literaturverzeichnis | Paetow et al. (2026) | II-14 | wie Nr. 23 | „DOI: nicht in den Quellen enthalten“ | Inventar 1a P3 | B | gering |
| 25 | II | Literaturverzeichnis | Wichmann et al. (2025) | II-14 | wie Nr. 23 | „DOI: nicht in den Quellen enthalten“ | Inventar 1a P2 | B | gering |
| 26 | II | Literaturverzeichnis | Sindermann et al. (2021) | II-14 | wie Nr. 23 | „Heft: nicht in den Quellen enthalten“ | Inventar 1a S2 | B | gering |
| 27 | II | Literaturverzeichnis | Wichmann et al. (2024) | II-14 | wie Nr. 23 | „Heft: nicht in den Quellen enthalten“ | Inventar 1a P1 | B | gering |
| 28 | II | Literaturverzeichnis | Wichmann et al. (2026) | II-14 | wie Nr. 23 | „Heft: nicht in den Quellen enthalten“ | Inventar 1a P5 | B | gering |

**Protokoll:** im eingefügten Text leer. Gezählt: Teil I 14, Teil II 14; fehlende Datensätze 5 (Nr. 7, 8, 9, 10, 14) [eigene Zählung]; geprüfte Zeilen nicht angegeben.

## Anhang B – Fehlerliste Durchlauf 2

| Nr. | Teil | Abschnitt/Tabelle | Zeile bzw. Item-ID bzw. H | Prüfpunkt | Befund | korrekte Angabe | Fundstelle | Typ | Schwere |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | I | 1a | P1, Bibliografie | I-2 | Die Fundstelle S. 15 ist der Block „Please cite as“ im Fließtext. Das ist weder Titelseite noch Kopf- oder Fußzeile. Dieselben Angaben stehen auf der Titelseite. | „Johannes Wichmann“, „Tanja Sophie Gesk“, „Michael Leyer“; Titel; „(JMIR Form Res 2024;8:e48600) doi: 10.2196/48600“ (S. 1) | P1, S. 1 | B | gering |
| 2 | I | 1a | S1a, Technologie | I-1 | Das Zitat „artificial intelligence“ hat keine Fundstelle. | „artificial intelligence“ (PDF-S. 1) | S1a, PDF-S. 1 | A | gering |
| 3 | I | 1a | S1b, Technologie | I-1 | „AI allgemein“ ist eine Paraphrase ohne Beleg. | „independent of the context“ (S. 7) | S1b, S. 7 | A | gering |
| 4 | I | 1a | P5, Technologie | I-1 | „virtuelle Meetings“ steht ohne Beleg. | „social interaction during virtual meetings on work engagement“ (S. 173) | P5, S. 173 | A | gering |
| 5 | I | 1a | P5, Phase | I-1 | „während Nutzung“ steht ohne Beleg. | während Nutzung: „employees had had sufficient time to experience virtual work environments“ (S. 178) | P5, S. 178 | A | gering |
| 6 | I | 1c S1, C4 | Modularität | I-1 | Die Seitenangabe S. 4 ist falsch. Der Satz steht in Abschnitt 2.3 auf S. 5. | „… (S1b, S. 5)“ | S1b, S. 5 | A | gering |
| 7 | I | 1c S1, C4 | Diskriminanzvalidität | I-8 | „nicht in den Quellen enthalten“ ist falsch. Es fehlt ein Datensatz: Eine Validierungsaussage zur Abgrenzung der Konstrukte liegt vor (Korrelationen in Table 2, S. 7). | „There are high correlations between the constructs of our questionnaire (i.e., AI literacy, AI Self-competency, Create AI, and AI Self-efficacy), but still enough differentiation that they can be understood as unique constructs.“ (Bezug: Faktoren 2. Ordnung) | S1b, S. 8; Table 2, S. 7 | C | mittel |
| 8 | I | 1c S2, C4 | Ausschlüsse | I-8 | Es fehlt ein Datensatz: Die Vertrauensitems wurden wegen Wortgleichheit mit ATAI 02 von der Validierung ausgeschlossen. Das ist relevant für Dimension 6. | „Please note that there is an overlap in the wording between the second item of the ATAI scale (“I trust …”) and the items on trust in the AI products.“ (Bezug: ATAI 02 / Trust-Items der Produkte) | S2, S. 113 | C | mittel |
| 9 | I | 1c S2, C4 | Validierungsaussagen | I-8 | Es fehlt ein Datensatz zur Einschränkung der Stichprobe. Er ist relevant für „Passung zum Fall“. Folgeänderung: Belegzitat in Tabelle A (ATAI) und in Offene Punkte Nr. 10 aufnehmen. | „the present samples mostly comprised rather young adults. Therefore, the generalizability of the results and applicability of the scale in older (or even younger) samples need to be investigated in future research.“ | S2, S. 116 | C | mittel |
| 10 | I | 1c S2; ⚠-Liste | ⚠ Nr. 1 (Ligaturen) | I-1 / I-10 | Die Ligaturen sind uneinheitlich wiedergegeben. Teils sind sie aufgelöst („five“ in C3 Szenario, „fifth“ in Tabelle B ATAI05), teils nicht („fve“, „artifcial“, „specifc“, „ft“ in 1b, C4 und C5). ⚠ Nr. 1 nennt nur „Artifcial“. | ⚠ Nr. 1 erweitern: „Die PDF-Extraktion von S2 verliert fi/ff-Ligaturen (‚Artifcial‘, ‚fve‘, ‚specifc‘, ‚ffth‘, ‚ft‘); im Inventar sind sie einheitlich aufgelöst.“ Danach alle S2-Zitate einheitlich auflösen. | S2, S. 109–116 | A | gering |
| 11 | I | 1c P3, C2 | TeC_Im_1 | I-10 | Die Modus-Abweichung ist nicht markiert: DE hat Konjunktiv („ermöglichen würde“), EN hat Indikativ („enables“). | „⚠ Abweichung (Modus)“ ergänzen und in die ⚠-Liste aufnehmen | D1 Fragebogen 3, Abschnitt Immersion | D | mittel |
| 12 | I | 1c P3, C2 | TeC_Im_2 | I-10 | Wie Nr. 11: DE „ausblenden könnte“, EN „allows me to“. | „⚠ Abweichung (Modus)“ ergänzen und in die ⚠-Liste aufnehmen | D1 Fragebogen 3, Abschnitt Immersion | D | mittel |
| 13 | I | 1c P3, C3 | Messverfahren | I-7 | Es fehlt ein Datensatz zum Pretest der Items und der Filterlogik. | „A pretest (n = 50) evaluated item clarity and filter logic.“ | P3, S. 322 | C | mittel |
| 14 | I | 1c P3, C4 | TTF | I-8 | Es fehlt eine Validierungsaussage zur Einschränkung des TTF-Werts. Folgeänderung: in Offene Punkte aufnehmen (Einschränkung des TTF-Werts im Fall). | „it reduces psychometric uniformity, since not all participants evaluate the same items. This limits cross-participant comparability and scale-based generalizability.“ (Bezug: TTF, Filterverfahren) | P3, S. 325 | C | mittel |
| 15 | I | 1c P3, C4 | Modellkennwerte | I-8 | Die Angaben sind unvollständig: Es fehlen SRMR und R² von TTF. | ergänzen: „The SRMR was 0.079 for the estimated model and 0.050 for the saturated model“ (S. 324); „The R² for TTF was 17.7%“ (S. 323) | P3, S. 323–324 | C | mittel |
| 16 | I | 1c P3, C5 | H1, H2, weitere Prädiktoren | I-9 | Die im Modell geprüften Moderatoren fehlen. | ergänzen: Alter, Geschlecht (Moderatoren): „No relevant effects were observed for the moderating roles of age and gender.“ | P3, S. 324 | C | mittel |
| 17 | II | Tabelle B | gesamte Tabelle | II-13 / Ausgabeformat | Die Spalten weichen vom Ausgabeformat ab. Die Spalten Block, Originalitem (Fundstelle), Antwortformat und (R) fehlen je Zeile. „Für alle Items gilt“ fasst Zellen zusammen. In den Blöcken 1, 3 und 6 fehlt eine eigene Spalte für das Originalitem. | Eine Zeile je Item mit genau diesen Spalten: Block \| Item-ID \| Konstrukt \| Originalitem (Fundstelle) \| finales Item \| Antwortformat \| Adaption \| (R) | Erstellungsprompt, Ausgabe Nr. 3, Formatregeln | G | gering |
| 18 | II | Tabelle B, Block 3 | 20 TTF-Items (wie Fehlerliste D1, Nr. 12) | II-7 / II-8 | Die ⚠-Abweichung „meine Aufgaben“ / „tasks“ ist nicht behandelt. Das ist ein Folgefehler aus Durchlauf 1, Nr. 12. | je Item: beide Fassungen nennen; Wahl der DE-Fassung [eigene Bewertung]; Pretest-Prüfpunkt (Bezug auf eigene vs. allgemeine Aufgaben) | Inventar C2 P3, ⚠ Nr. 11 | E | gering |
| 19 | II | Tabelle B, Block 3 | alle TTF-Items, Sprachfassung | II-8 | Die Wahl „kann“ statt „could“ ist nicht als [eigene Bewertung] gekennzeichnet. | „… wird gewählt [eigene Bewertung]“ | Erstellungsprompt 2.2, Originalitem | E | gering |
| 20 | II | Tabelle B, Block 1 | Aufgabenbeschreibung Creativity | II-8 | ⚠ Nr. 9 ist beim übernommenen Text nicht dokumentiert: Die EN-Fassung ist eine Kopie von Planning. | „DE-Fassung gewählt, EN-Fassung ist Kopie der Planning-Beschreibung (⚠ Nr. 9) [eigene Bewertung]; Pretest-Prüfpunkt“ | Inventar C3 P3, ⚠ Nr. 9 | E | gering |
| 21 | II | Tabelle B, Block 5 | Instruktion PERF | II-8 | ⚠ Nr. 15 (DE/EN) ist nicht dokumentiert. Genannt ist nur die Grammatik. | beide Fassungen nennen; Wahl der DE-Fassung [eigene Bewertung]; Pretest-Prüfpunkt | Inventar C3 P3, ⚠ Nr. 15 | E | gering |
| 22 | II | Tabelle B, Polung | Begründung Block 1 | II-12 / II-2 | Der Kennwert „all outer loadings … exceeding the 0.708 threshold“ gilt nicht für TC_Performance_3. Das Item wurde wegen niedriger Ladung entfernt (Regel 4). | „Block 1 außer TC_Performance_3: Kennwert S. 323; D1-Q3-TC_Performance_3: als Skala nicht validiert (entfernt, S. 323)“ | Inventar C4 P3 | F | schwer |
| 23 | II | Tabelle B, Blöcke 1 und 3 | Spalte Konstrukt, TC/TTF_Performance_1–3 | II-3 / II-13 | Der Konstruktname „Execution“ weicht vom Inventar ab („Execution/Performance“, Regel 6). | „TC Execution/Performance“ bzw. „TTF Execution/Performance“ | Inventar C2 P3 | F | schwer |
| 24 | II | Tabelle A | Dimension 1 (MAILS), Theorie/Instrument | II-3 | Die Herkunft laut C2 fehlt. Sie ist je Facette angegeben. | „MAILS (Carolus et al., 2023); Herkunft je Facette laut C2, z. B. Use & Apply: Ng et al. (2022, zit. n. Carolus et al., 2023)“ | Inventar C2 S1; S1b, S. 9–10 | E | gering |
| 25 | II | Tabelle A | Dimension 1, verworfene Alternativen | II-2 | P4 steht ohne Belegzitat (2.1). | P4: Belegzitat aus 1b (S. 8) und „Antwortskala nicht in den Quellen enthalten“ | Inventar 1b, Schritt 4 | E | gering |
| 26 | II | Tabelle A | Dimension 2, ATAI Fear, verworfene Alternativen | II-2 | P1 und P2 stehen ohne Belegzitate. | Belegzitate aus 1b ergänzen (P1, S. 1; P2, S. 961) | Inventar 1b, Schritt 4 | E | gering |
| 27 | II | Tabelle A | Dimension 5 (BI), verworfene Alternativen | II-2 | P1, P2 und P4 stehen ohne Belegzitate. | Belegzitate aus 1b ergänzen (P1, S. 1; P2, S. 961; P4, S. 8) | Inventar 1b, Schritt 4 | E | gering |
| 28 | II | Tabelle A | Dimension 6, verworfene Alternativen | II-2 / II-4 | „ATAI 02“ ist ein Teil der ausgewählten Quelle S2 und keine verworfene Quelle (2.1). P2 (D1 Q2 Trust) fehlt. Belegzitate fehlen. | „P4 Trust: Format ungeeignet, Beleg S. 8; P2 (D1 Q2 Trust): Beleg S. 961“. ATAI 02 nur unter „Passung“ [eigene Bewertung] mit Beleg aus Nr. 8 (S2, S. 113) | Inventar 1b, Schritt 3–4 | E | gering |
| 29 | II | Tabelle A | Dimension 7, verworfene Alternativen | II-2 | P1 und P2 stehen ohne Belegzitate. | Belegzitate aus 1b ergänzen (P1, S. 1; P2, S. 961) | Inventar 1b, Schritt 4 | E | gering |
| 30 | II | Tabelle A | PERF und BI, Passung | II-13 | Der Verweis „wie Zeile 3“ ist mehrdeutig, denn gezählt ist Zeile 3 = ATAI Fear. | „wie Dimension 3 (TTF)“ | Tabelle A | G | gering |
| 31 | II | Tabelle A ↔ Offene Punkte | TTF, Einsatzfelder ↔ Nr. 4 | II-13 | Widerspruch: Tabelle A sagt „Texte entwerfen → Creativity nur teilweise“, Offene Punkte Nr. 4 sagt „kein Teilbereich deckt sie ab“. | Beide Stellen gleich formulieren: „Texte entwerfen: nur teilweise Creativity [eigene Bewertung]; zusammenfassen: kein Teilbereich“ | Tabelle A; Offene Punkte Nr. 4 | G | gering |

**Protokoll:** Durchlauf 2 | 319 | 156 | 16 | 15 | 7 (Nr. 7, 8, 9, 13, 14, 15, 16)

## Anhang C – Fehlerliste Durchlauf 3

| Nr. | Teil | Abschnitt/Tabelle | Zeile bzw. Item-ID bzw. H | Prüfpunkt | Befund | korrekte Angabe | Fundstelle | Typ | Schwere |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | I | 1c S1, C4 | Ausschluss; Itemebene | I-1 | Die Fundstelle „(S. 6)“ hat kein Dokumentkürzel. Die Quelle S1 besteht aber aus zwei Dokumenten (S1a, S1b). | „(S1b, S. 6)“ bei beiden Angaben | S1b, S. 6 | A | gering |
| 2 | I | 1c S1, C4 | Validierungsaussagen | I-8 | Fehlender Datensatz: Die Einschränkung zur Stichprobe fehlt. | Validierungsaussage (Bezug: Stichprobe, alle Facetten): „Our sample was collected online and is specific to German-speaking individuals who live in Germany or Austria.“ | S1b, S. 8 | C | mittel |
| 3 | I | 1c P3, C4 | Validierungsaussagen | I-8 | Fehlender Datensatz: Die Einschränkung durch die beschreibenden Stimuli fehlt. Sie betrifft alle Konstrukte. | Validierungsaussage (Bezug: alle Konstrukte, Stimulus): „Because VR was introduced via descriptive stimuli rather than live experiences, validity and generalizability are limited.“ | P3, S. 320 | C | mittel |
| 4 | I | 1c P3, C3 | Instruktionstext TTF | I-7, I-10 | Fehlender Datensatz: Die EN-Instruktion enthält einen Kontextzusatz, den die DE-Fassung nicht hat. Die Abweichung ist nicht markiert. | ⚠ Abweichung: EN „Imagine you are using Virtual Reality in your professional context.“ / DE „Stellen Sie sich vor, Sie arbeiten mit Virtual Reality.“ | D1, Fragebogen 3, Abschnitt TTF | C | mittel |
| 5 | I | 1c P3, C2 | TC_Intellective_1 | I-10 | DE und EN weichen ab, die Abweichung ist nicht markiert: DE „eindeutig richtige“, EN „objectively correct“. | „⚠ Abweichung (DE ‚eindeutig richtige‘ / EN ‚objectively correct‘)“ | D1, Fragebogen 3, TC Intellective | D | mittel |
| 6 | I | 1c P3, C2 | TC_Intellective_2 | I-10 | Der Verstärker „eindeutig“ steht nur in der DE-Fassung. Die Abweichung ist nicht markiert. | „⚠ Abweichung (DE ‚eindeutig bestimmbar‘ / EN ‚can be determined‘)“ | D1, Fragebogen 3, TC Intellective | D | mittel |
| 7 | I | 1c P3, C2 | TC_Judgmental_1 | I-10 | DE und EN weichen ab, die Abweichung ist nicht markiert. | „⚠ Abweichung (DE ‚eindeutig richtige Antwort‘ / EN ‚objectively correct answers‘)“ | D1, Fragebogen 3, TC Judgment | D | mittel |
| 8 | I | 1c P3, C2 | TTF_Intellective_1 | I-10 | DE und EN weichen ab, die Abweichung ist nicht markiert. | „⚠ Abweichung (DE ‚eindeutig richtige Lösung‘ / EN ‚objectively correct solutions‘)“ | D1, Fragebogen 3, TTF Intellective | D | mittel |
| 9 | I | 1c P3, C2 | TTF_Intellective_2 | I-10 | Der Verstärker „eindeutig“ steht nur in der DE-Fassung. Die Abweichung ist nicht markiert. | „⚠ Abweichung (DE ‚eindeutig bestimmbar‘ / EN ‚can be determined‘)“ | D1, Fragebogen 3, TTF Intellective | D | mittel |
| 10 | I | 4. ⚠-Liste | – | I-10 | Die Einträge zu den Befunden 4–9 fehlen. | neue Nr. 21: TTF-Instruktion DE/EN (Kontextzusatz); neue Nr. 22: „eindeutig“ DE vs. „objectively“/ohne Entsprechung EN bei TC_Intellective_1, TC_Intellective_2, TC_Judgmental_1, TTF_Intellective_1, TTF_Intellective_2 | D1, Fragebogen 3 | D | mittel |
| 11 | II | Block-Instruktionen, Block 3 | Instruktion | II-7, II-8 | Die DE/EN-Abweichung (Befund 4) ist weder dokumentiert noch begründet. Es fehlt ein Pretest-Prüfpunkt. | ⚠ Abweichung nennen; Wahl der DE-Fassung begründen: „Erhebung auf Deutsch (P3, S. 322)“ [eigene Bewertung]; Pretest-Prüfpunkt: Bezug auf den Arbeitskontext | Inventar 1c P3, C3 | E | gering |
| 12 | II | Tabelle B | D1-Q3-TC_Intellective_1 | II-7 | Der Verstärker „eindeutig“ bleibt ohne zitierten Kennwert. Die DE/EN-Abweichung ist nicht vermerkt. [eigene Bewertung: „eindeutig“ = Verstärker] | Adaption ergänzen: „Verstärker bleibt; Kennwert: ‚all outer loadings for reflective constructs exceeding the 0.708 threshold‘ (S. 323); ⚠ Abweichung DE/EN, DE gewählt (Erhebung auf Deutsch, S. 322) [eigene Bewertung]; Pretest-Prüfpunkt“ | P3, S. 322–323; Befund 5 | E | gering |
| 13 | II | Tabelle B | D1-Q3-TC_Intellective_2 | II-7 | Der Kennwert ist nur für das Begriffspaar zitiert, nicht für den Verstärker „eindeutig“. Die DE/EN-Abweichung ist nicht vermerkt. | wie Nr. 12 | P3, S. 323; Befund 6 | E | gering |
| 14 | II | Tabelle B | D1-Q3-TC_Judgmental_1 | II-7 | wie Nr. 12 | wie Nr. 12 | P3, S. 323; Befund 7 | E | gering |
| 15 | II | Tabelle B | D1-Q3-TTF_Intellective_1 | II-7 | Für den Verstärker liegt kein Kennwert vor (Einzelindikator). Es fehlen das inhaltliche Belegzitat und ein Pretest-Prüfpunkt. Die DE/EN-Abweichung ist nicht vermerkt. | „Verstärker bleibt; kein Kennwert; Beleg: ‚intellective tasks, which require objectively correct solutions‘ (S. 320); ⚠ Abweichung DE/EN, DE gewählt [eigene Bewertung]; Pretest-Prüfpunkt“ | P3, S. 320; Befund 8 | E | gering |
| 16 | II | Tabelle B | D1-Q3-TTF_Intellective_2 | II-7 | Der Beleg deckt nur das Begriffspaar ab, nicht den Verstärker „eindeutig“. Die DE/EN-Abweichung ist nicht vermerkt. | wie Nr. 15 | P3, S. 320; Befund 9 | E | gering |
| 17 | II | Tabelle B | D1-Q3-TTF_Judgmental_1 | II-7 | Für den Verstärker „eindeutig richtige Antwort“ fehlen das Belegzitat und der Pretest-Prüfpunkt. EN „clearly correct“ entspricht dem DE-Wortlaut, daher besteht hier keine ⚠-Abweichung. | „Verstärker bleibt; kein Kennwert; Beleg: ‚judgmental tasks, which involve subjective decisions among multiple alternatives‘ (S. 320); Pretest-Prüfpunkt“ | P3, S. 320 | E | gering |
| 18 | II | Tabelle A (Dim. 3–5, Spalte „validiert“) und Offene Punkte Nr. 5 | TTF, PERF, BI | II-9, II-13 | Die Validierungsaussage aus Befund 3 fehlt in Teil II. Dadurch ist die Einschränkung der Urteilsbasis unvollständig belegt. | nicht im eingefügten Text enthalten (Zeile abgeschnitten); umgesetzt laut Fassung D3: Zitat „Because VR was introduced via descriptive stimuli rather than live experiences, validity and generalizability are limited.“ (P3, S. 320) in Tabelle A (Dim. 3–5) und Offene Punkte Nr. 5 | nicht im eingefügten Text enthalten | G | gering |

**Protokoll:** nicht eingefügt. Gezählt: Teil I 10, Teil II 8; fehlende Datensätze 3 (Nr. 2, 3, 4) [eigene Zählung]; geprüfte Zeilen nicht angegeben.

## Anhang D – Fehlerliste Kontrolllauf (dieser Chat)

| Nr. | Teil | Abschnitt/Tabelle | Zeile bzw. Item-ID bzw. H | Prüfpunkt | Befund | korrekte Angabe | Fundstelle | Typ | Schwere |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | I | 1a | S1a, Bibliografie | I-2 | Angabe stammt aus der Literaturangabe am Ende von PDF-S. 3 (Fließtext nach der Auswertungsregel, erscheint nicht auf PDF-S. 1–2); weder Titelseite noch Kopf- oder Fußzeile [eigene Bewertung]. | Kopfzeile: „MAILS Carolus, Koch, et al., 2023“ (PDF-S. 1–3); übrige Angaben siehe S1b (zugehörige Quelle); Heft: nicht in den Quellen enthalten | S1a, PDF-S. 1–3; S1b, S. 1 | B | gering |
| 2 | I | 1a | S1b, Bibliografie (Autor:innen) | I-2 | Autor:innen nicht wörtlich von der Titelseite, sondern als Initialen im Format von S1a. | „Astrid Carolus“, „Martin J. Koch“, „Samantha Straka“, „Marc Erich Latoschik“, „Carolin Wienrich“ | S1b, S. 1 | B | gering |
| 3 | I | 1a | P4: Stichprobe, Technologie, Phase | I-1 | „S. 1“ angegeben; erste Artikelseite trägt keine gedruckte Seitenzahl, PDF-S. 1 ist das Deckblatt – Seite geschätzt. | „(PDF-S. 2)“ bei allen drei Zitaten | P4, PDF-S. 2 | A | gering |
| 4 | I | 1c S1, C4 | Validierungsaussagen | I-8 | Fehlender Datensatz: fehlende externe Validierung. | Validierungsaussage (Bezug: Konstruktvalidität MAILS): „Also, it was not possible to use an already existing and validated instrument on AI literacy to validate our questionnaire, as would be the gold standard for scale development.“ | S1b, S. 8 | C | mittel |
| 5 | I | 1c S2, C4 | Ausschlüsse (Item 05) | I-8 | Fehlender Datensatz: Teil II stützt die Entscheidung zu Item 05 auf diese Aussage, sie steht nicht im Inventar. | Bezug Item 05 / Fear: „In other samples that include more employed people being at a risk of losing their jobs due to AI progress, the fifth item might load more strongly on the ATAI Fear factor.“ | S2, S. 116 | C | mittel |
| 6 | I | 1c S2, C4 | Validierungsaussagen | I-8 | Fehlender Datensatz: Einschränkung zur Itemkonstruktion. | Validierungsaussage (Bezug: beide Skalen): „However, the items were not extracted out of a bigger item pool based on an exploratory factorial analysis/PCA. This might be seen as a shortcoming of the questionnaire.“ | S2, S. 116 | C | mittel |
| 7 | I | 1c P3, C3 | Aufgabenbeschreibung TC Intellective | I-10 | DE/EN-Abweichung nicht markiert; „eindeutig“ nur DE (Muster wie ⚠ Nr. 22). | „⚠ Abweichung (DE ‚zu einer eindeutig überprüfbaren Antwort‘ / EN ‚to arrive at a verifiable answer‘)“ | D1, Fragebogen 3, TC Intellective | D | mittel |
| 8 | I | 1c P3, C3 | Blockfrage TTF Execution | I-10 | DE/EN-Abweichung nicht markiert; nur DE grenzt auf „klar definierte“ Aufgaben ein. | „⚠ Abweichung (DE ‚bei der Durchführung klar definierter Aufgaben‘ / EN ‚in performing execution or performance tasks‘)“ | D1, Fragebogen 3, TTF Execution | D | mittel |
| 9 | I | 4. ⚠-Liste | – | I-10 | Einträge zu den Befunden 7 und 8 fehlen. | neue Nr. 23: TC-Intellective-Beschreibung, „eindeutig“ nur DE; neue Nr. 24: TTF-Execution-Blockfrage, „klar definierter“ nur DE | D1, Fragebogen 3 | D | mittel |
| 10 | I | 1c P3, C4 | Kennwerte formative Konstrukte | I-8 | Fehlender Datensatz: VIF und Gewichte für TC und TeC. | Bezug TC, TeC: „For formative constructs (TC, TeC), variance inflation factor (VIF) values remained below 3.0 […] only TC_Contest and TeC_SP had relevant weights (p < .001).“ | P3, S. 323 | C | mittel |
| 11 | I | 1c P3, C4 | Validierungsaussagen | I-8 | Fehlender Datensatz: Einschränkung zur Stichprobe (für S1, S2 aufgenommen, für P3 nicht). | „Second, the sample consisted of German-speaking Clickworker users, which may introduce cultural and self-selection bias.“ | P3, S. 326 | C | mittel |
| 12 | II | 1. Instruktion, Block 2 | „Allgemeine Beschreibung“ | II-9 | „künstlicher Intelligenz“ kommt in allen ATAI-Items vor (Block 6); „beruht auf KI“ ist zudem kein Einsatzfeld (2.4). | „Microsoft Copilot ist ein Programm. Copilot kann Texte entwerfen und vorhandene Texte zusammenfassen.“ | Erstellungsprompt 2.4; Inventar C2 S2 | F | schwer |
| 13 | II | Tabelle B | S2-ATAI05 | II-1 | Belegzitat steht nicht im Inventar und ist ohne „[…]“ gekürzt. | nach Befund 5: „… the fifth item might load more strongly on the ATAI Fear factor.“ (S2, S. 116); zusätzlich „validierte Skala vollständig (Regel 10)“ | Inventar C4 S2 | F | schwer |
| 14 | II | Tabelle A | Dim. 2, ATAI Fear, Passung | II-2 / II-5 | „Item 05 bleibt wegen beschäftigter Zielgruppe“ ist eine Entscheidung ohne Belegzitat; tragender Grund ist Regel 10. | „Item 05 bleibt: validierte Skala vollständig (Regel 10). Zur Zielgruppe: ‚In other samples that include more employed people […]‘ (S2, S. 116); Pretest-Prüfpunkt: Ladung in der Zielgruppe“ | Inventar C4 S2 | E | gering |
| 15 | II | Block-Instruktionen, Block 1 | Aufgabenbeschreibung Intellective | II-8 | Abweichung aus Befund 7 beim übernommenen Text nicht dokumentiert. | „⚠ Abweichung (⚠ Nr. 23); DE gewählt (P3, S. 322) [eigene Bewertung]; Pretest-Prüfpunkt: Verständnis von ‚eindeutig‘“ | Inventar C3 P3 | E | gering |
| 16 | II | Block-Instruktionen, Block 3 | Überschrift „Durchführung klar definierter Aufgaben“ | II-7 / II-8 | Abweichung aus Befund 8 nicht dokumentiert. | „⚠ Abweichung (⚠ Nr. 24); DE gewählt (P3, S. 322) [eigene Bewertung]; Pretest-Prüfpunkt: Passung der Überschrift zu D1-Q3-TTF_Performance_2 und _3“ | Inventar C3 P3 | E | gering |
| 17 | II | Tabelle B | D1-Q3-TC_Performance_1 | II-7 | Verstärker „klar“ bleibt ohne Kennwert (analog „eindeutig“, Fehlerliste 3 Nr. 12) [eigene Bewertung: „klar“ = Verstärker]. | „Verstärker ‚klar‘ bleibt; Kennwert: ‚all outer loadings for reflective constructs exceeding the 0.708 threshold‘ (S. 323); Pretest-Prüfpunkt“ | P3, S. 323 | E | gering |
| 18 | II | Tabelle B | D1-Q3-TTF_Performance_1 | II-7 | Wie Nr. 17, aber ohne Kennwert (Einzelindikator); Belegzitat und Pretest-Prüfpunkt fehlen. | „Verstärker ‚klar‘ bleibt; kein Kennwert; Beleg: ‚performance tasks, which require precise, coordinated physical execution under defined conditions‘ (S. 320); Pretest-Prüfpunkt“ | P3, S. 320 | E | gering |
| 19 | II | Gemeinsame Anmerkungen, Polung | Block 6 | II-12 | Einheitliche Polung mit Faktorstruktur statt mit Validierungskennwert begründet (2.2, Polung). | „Block 6: Ladungen Deutschland 02 = 0.69, 04 = 0.71, 01 = 0.83, 03 = 0.64, 05 = 0.42 (Table 2, S. 113); α = 0.65 / 0.66 (S. 114)“ | Inventar C4 S2 | E | gering |
| 20 | II | Offene Punkte Nr. 10; Tabelle A, Dim. 3–5 | P3 | II-13 | Folgeänderung aus Befund 11: Stichprobeneinschränkung von P3 fehlt in Teil II. | ergänzen: „P3: ‚the sample consisted of German-speaking Clickworker users, which may introduce cultural and self-selection bias‘ (S. 326)“ | Inventar C4 P3 | G | gering |
| 21 | II | Literaturverzeichnis | Carolus et al. (2023) | II-14 | Heftangabe „(2)“ stammt aus der Literaturangabe in S1a (Befund 1), nicht aus einer zulässigen Stelle in 1a. | „Computers in Human Behavior: Artificial Humans, 1, Article 100014. Heft: nicht in den Quellen enthalten.“ | Inventar 1a S1b | B | gering |
| 22 | II | Tabelle D; Abschluss | I-2, I-8, I-10, II-1, II-7, II-9, II-12, II-13, II-14; Protokoll Durchlauf 1 | II-13 | Status „erfüllt“/„korrigiert“ durch Befunde 1–21 widerlegt; Zahlen für Durchlauf 1 jetzt aus eingefügter Fehlerliste ablesbar. | Tabelle D nach Korrektur neu erstellen; Protokoll Durchlauf 1: Teil I 14, Teil II 14 | Fehlerlisten D1–D3 | G | gering |

**Protokoll:** Kontrolllauf nach Durchlauf 3 | 306 | 142 | 11 | 11 | 5 (Nr. 4, 5, 6, 10, 11)

## Anhang E – Erstellungsprompt V8 (= V8.1)

*Wortlaut aus dem Repo (Datei V8_1); inhaltlich identisch mit Projektdokument „V8 Prompt“ (Abschnitt 2).*

### Prompt V8 – Erstellungsprompt: Quelleninventar und Fragebogen (KI-Readiness)

Dieser Prompt erstellt Inventar und Fragebogen. Die Prüfung erfolgt danach mit dem Prüfprompt V8.2 in einem neuen Chat.

#### Fall-Parameter (vom Menschen festgelegt, austauschbar)
- Technologie: Microsoft Copilot
- Zielgruppe: Beschäftigte ohne KI-Fachausbildung
- Phase: vor der Einführung
- Untersuchungsziel: KI-Readiness der Beschäftigten für die geplante Nutzung
- Fragebogensprache: Deutsch
- Einsatzfelder der Technologie: Texte entwerfen, zusammenfassen, Daten auswerten, Abläufe planen

#### Input
Projektquellen (Paper, Itemkataloge, Itemblätter).

#### Rolle
Du bist Expertin für Fragebogenkonstruktion, Technologieakzeptanz und KI-Readiness. Du arbeitest in zwei getrennten Schritten:
- **Schritt 1:** Du analysierst die Quellen, wählst die geeigneten aus und erstellst ein Inventar. Hier extrahierst du nur.
- **Schritt 2:** Du erstellst den Fragebogen ausschließlich aus diesem Inventar.

Beginne Schritt 2 erst, wenn Schritt 1 vollständig ausgegeben und geprüft ist.

---

#### Goldene Regeln (gelten für beide Schritte)
1. **Wörtlich mit Fundstelle.** Jede Angabe aus einer Quelle ist ein wörtliches Zitat oder ein Zahlenwert, der genau so im Dokument steht. Fundstelle: Dokumentkürzel, gedruckte Seite, ggf. Tabelle (ohne gedruckte Seite: „PDF-S. n“).
2. **Kein Vorwissen.** Ergänze nichts aus deinem Wissen, auch nicht bei Quellen, die du zu kennen glaubst (z. B. Heftnummer, Autor:innen, Itemwortlaut, Kennwerte). Fehlt eine Angabe nach Durchsuchen der ganzen Quelle (inkl. Tabellen, Methodenteil, Anhang): „nicht in den Quellen enthalten“. Eigene Texte kennzeichnest du mit [Modellwissen], eigene Einschätzungen mit [eigene Bewertung].
3. **Belegzitat vor Entscheidung.** Jede Entscheidung (Auswahl, Ausschluss, Teilauswahl, Skalenumstellung, Beibehaltung eines Originalitems, Änderung der Blockreihenfolge) braucht ein wörtliches Belegzitat (max. 40 Wörter, mit Fundstelle), das die Entscheidung inhaltlich trägt. Schreibe zuerst das Zitat, dann die Entscheidung. Paraphrasen gelten nicht als Beleg. Ohne tragendes Zitat: [eigene Bewertung]. Für Abweichungen von einer validierten Skala genügt [eigene Bewertung] nicht (Regel 10).
4. **Geltungsbereich prüfen.** Eine Entscheidung der Quelle überträgst du nur, wenn das Belegzitat ausdrücklich das Konstrukt nennt, auf das du sie anwendest. Nennt es ein anderes Konstrukt, eine andere Rolle (z. B. Prädiktor statt Filter) oder eine andere Technologie, gilt die Entscheidung nicht. Ein Beleg gilt nur für die Ebene, die er nennt (z. B. Modularität für Subskalen, nicht für einzelne Items), und nur für das Instrument, aus dem er stammt.
5. **Ein Konstrukt = eine Quelle = eine Theorie.** Definition, Items und Hypothese eines Konstrukts stammen aus derselben Quelle. Mische niemals Quellen, auch nicht bei ähnlichen Konstrukten (z. B. „Intention to use“ aus verschiedenen Quellen). Ein Itemkatalog gilt zusammen mit dem Paper, zu dem er gehört, als eine Quelle.
   - **Theorie eines Konstrukts** ist die Herkunftsangabe der Quelle für genau dieses Konstrukt (z. B. „adapted from UTAUT“), nicht das Rahmenmodell des Papers. Ein Paper kann Konstrukte aus mehreren Theorien enthalten.
   - Für Hypothesen gilt Regel 11.
6. **Konstruktname.** Verwende den Konstrukt- bzw. Faktornamen der Quelle. Nur wenn die Items etwas anderes messen als der Theoriebegriff (z. B. Benevolence gemessen als Unheimlichkeit), benennst du das Konstrukt nach dem Iteminhalt und nennst den Theoriebegriff in Klammern. Ein Name enthält keine Begriffspaare und keine Begriffe anderer Theorien oder Konstrukte des Fragebogens.
7. **Konstrukt treu übernehmen.** Ein adaptiertes Item misst dasselbe Konstrukt auf derselben Bezugsebene (Organisation vs. Individuum, „wir“ vs. „ich“). Weicht die Zielgruppe der Quelle vom Fall ab, nenne das in Tabelle A unter „Passung zum Fall“.
8. **Nichts voraussetzen.** Kein Item setzt Erfahrung mit der Technologie voraus, auch nicht in Nebensätzen: kein Indikativ, der Nutzung oder eine dabei entstehende Emotion voraussetzt. Kein Item setzt eine Rolle oder Entscheidungsbefugnis voraus, die die Zielgruppe nicht hat.
9. **Korrekt vor vollständig.** Ist eine Vorgabe nicht regelkonform erfüllbar (z. B. keine geeignete Quelle, Kriterium fehlt, kein Teilbereich deckt ein Einsatzfeld ab, validierte Sprachfassung fehlt), erfinde keinen Ersatz. Erstelle den regelkonformen Teil und führe die Vorgabe unter „Offene Punkte“ mit Grund auf.
10. **Validierte Skalen unverändert.** Validierte Skalen nur vollständig, im Originalformat und in der validierten Sprachfassung übernehmen; jede Abweichung nur mit wörtlichem Quellenbeleg, sonst unterlassen.
    - **Validiert** ist eine Skala bzw. Subskala, für die C4 Kennwerte oder eine Validierungsaussage zu genau dieser Skala nennt.
    - **Vollständig:** alle Items der finalen Fassung (2.2).
    - **Originalformat:** Stufenzahl, Anker und Urteilstyp der Quelle, ohne Zusatzoptionen (2.5).
    - **Validierte Sprachfassung:** der Wortlaut in der Erhebungssprache laut C3. Ist die Erhebungssprache die Fragebogensprache und fehlt dieser Wortlaut im Inventar, verwendest du die Skala nicht und führst unter „Offene Punkte“ auf: „validierte Fassung beschaffen“ (Regel 9). Weicht die Erhebungssprache von der Fragebogensprache ab oder ist sie nicht in den Quellen enthalten, ist eine Übersetzung zulässig: Code Ü, Verfahren dokumentiert (Vorwärtsübersetzung und unabhängige Rückübersetzung), als nicht validiert ausgewiesen, Eintrag unter „Offene Punkte“.
    - Ohne Beleg zulässig sind nur die erlaubten Änderungen aus 2.2; auch sie werden dokumentiert.
11. **Hypothesen nur innerhalb einer Theorie.** Hypothesen nur aufnehmen, wenn Prädiktor- und Kriteriumsitems aus derselben Theorie stammen (Herkunftsangabe laut C2, Regel 5). Das gilt auch, wenn die Quelle die Hypothese geprüft hat. Ist die Herkunft eines der beiden Konstrukte nicht in den Quellen enthalten, gilt die Theoriegleichheit als nicht belegt. Nicht aufgenommene Hypothesen führst du unter „Offene Punkte“ mit der Herkunft beider Konstrukte auf.

**Rangfolge bei Regelkonflikten:** 1. Nichts erfinden (Regeln 1–4, 9) → 2. Konstrukttreue und Validierung (5–7, 10, 11) → 3. Keine Voraussetzungen (8) → 4. Sprachliche Anpassung. Löse einen Konflikt nie stillschweigend, sondern dokumentiere ihn beim betroffenen Item.

---

#### Schritt 1 – Quellenanalyse und Inventar

##### 1a Formatanalyse (alle Quellen)
Zähle die vorliegenden Dateien und nenne die Zahl. Liegt eine Datei nur als Kopie vor (z. B. Zusatz „- Kopie“), ist sie die Quelle. Prüfe auf Inhaltsgleichheit nur, wenn Original und Kopie beide vorliegen.

Prüfe für jede Quelle, welche Bestandteile für einen Fragebogen sie wörtlich enthält.

Kürzel | Dokumenttyp (Itemkatalog / Itemblatt / Validierungsstudie / Modellstudie mit Hypothesen) | zugehörige Quelle (Katalog ↔ Paper) | Bibliografie (alle Autor:innen, Jahr, Titel, Zeitschrift/Proceedings, Jahrgang, Heft, Seiten/Artikelnr., DOI – wörtlich) | Stichprobe/Zielgruppe | Technologie/Gegenstand | Phase (vor/während/nach Nutzung) | Konstrukte (Originalname + Rolle: Prädiktor/Kriterium/Filter/Einzelindikator) | Items wörtlich (DE/EN) | Antwortskala | Kennwerte (Ladung, α, AVE o. Ä.) | geprüfte Hypothesen | Messverfahren (Filter, Szenario, Itemstamm)

Die letzten fünf Spalten füllst du jeweils mit „ja (Fundstelle)“ oder „nein“.

##### 1b Auswahl
1. **Format:** Eine Quelle ist verwendbar, wenn sie allein oder zusammen mit ihrem Katalog wörtliche Items und eine Antwortskala enthält, dazu Kennwerte oder geprüfte Hypothesen. Sonst verwirfst du sie mit „Format ungeeignet“.
2. **Readiness-Dimensionen:** Leite die Dimensionen aus den Konstrukten der verwendbaren Quellen und dem Untersuchungsziel ab, benenne jede in einem Satz und kennzeichne sie als [eigene Bewertung]. Die Dimensionen gliedern den Fragebogen; eine eigene Definition von KI-Readiness formulierst du nicht.
3. **Passung je Dimension:** Prüfe jede Dimension einzeln. Wähle je Dimension unter den verwendbaren Quellen genau die eine, deren Theorie bzw. Instrument am besten zu Dimension, Zielgruppe, Technologie und Phase passt. Eine Quelle kann mehrere Dimensionen abdecken; eine Dimension wird nie aus mehreren Quellen gemessen (Regel 5). Verwirf eine Quelle nicht deshalb, weil sie nur eine Dimension abdeckt.
4. Je Quelle: ausgewählt / verworfen | Dimension(en) | Grund (Format oder Passung) | Belegzitat aus 1a | Begründung in einem Satz [eigene Bewertung].
5. Passt zu einer Dimension keine Quelle: „keine passende Quelle für Dimension …“ (Regel 9). Die übrigen Dimensionen erstellst du trotzdem.

##### 1c Vollinventar (nur ausgewählte Quellen, jede einzeln, mit zugehörigem Katalog)
- **C1 Definitionen:** Konstrukt | Definition wörtlich oder „nicht in den Quellen enthalten“ | primär oder Sekundärzitat im Format „Primärwerk (Jahr, zit. n. Quelle, Jahr)“ (Zuschreibung laut Literaturverzeichnis der Quelle) | Fundstelle
- **C2 Items:** Item-ID wie in Quelle/Katalog (ohne Nummer: „Position n“) | Konstrukt | Wortlaut DE | Wortlaut EN | Itemstamm | Herkunft der Items laut Quelle (wörtlich, z. B. „adapted from …“, mit zitiertem Werk; sonst „nicht in den Quellen enthalten“) | Fundstelle (Katalog und Paper)
- **C3 Messverfahren:** Antwortskala je Konstrukt (Stufenzahl, Anker wörtlich) | Begründung der Skala | Aussagen zu anderen Skalierungen | Filterfragen und Filterregel | Szenario/Technologiebeschreibung (Umfang, Gliederung, Abbildungen) | Instruktions- und Blockfragetexte wörtlich | Blockreihenfolge | Erhebungssprache
- **C4 Modell:** Konstrukt | Rolle | Aggregationsregel (mit Bezug: für welches Instrument bzw. welche Skala) | Ausschlüsse (was, betroffenes Konstrukt laut Quelle oder „Bezug nicht genannt“, Grund) | Kennwerte mit Bezug (Skala und deren Itemzahl): Itemebene (Ladungen), Skalenebene (α, CR, AVE), Diskriminanzvalidität (z. B. HTMT), Validierungsaussagen (z. B. „all items loaded significantly“); sonst „keine Kennwerte“
- **C5 Hypothesen:** H-Nr. | Hypothese wörtlich | Prädiktor | Kriterium | Herkunft Prädiktor / Kriterium (aus C2) | Ergebnis (β, p, bestätigt/nicht bestätigt) | weitere Prädiktoren im Modell | Fundstelle

Weichen Fassungen voneinander ab (Katalog vs. Paper, DE vs. EN, Text vs. Tabelle, Filter- vs. Fit-Item), nenne beide mit Fundstelle und markiere sie mit „⚠ Abweichung“. Entscheide in Schritt 1 nicht, welche gilt.

##### Prüfung Schritt 1
Prüfe jedes Zitat zeichengenau an der Fundstelle. Was du nicht sicher prüfen kannst, markierst du mit „⚠ nicht geprüft“.

---

#### Schritt 2 – Fragebogenerstellung
Jede Angabe im Fragebogen stammt aus Schritt 1 (im Folgenden „Inventar“). Was nicht im Inventar steht, kommt nicht vor. Du verwendest nur Quellen, die in 1b ausgewählt sind und ein Vollinventar haben.

##### 2.1 Konstrukte
- **Auswahl:** Übernimm die Auswahl und die Zuordnung zu Dimensionen aus 1b unverändert. Verworfene Alternativen sind die in 1b verworfenen Quellen mit ihren Belegzitaten, keine Teilkonstrukte derselben Quelle.
- **Subskalen:** Ein Instrument mit mehreren Subskalen (z. B. Facetten) darf mit einzelnen Subskalen eingehen, wenn ein Belegzitat zeigt, dass die Quelle diese Subskalen getrennt auswertet (z. B. Mittelwert je Facette). Ordne jede Subskala genau einer Dimension zu und begründe die Zuordnung [eigene Bewertung]. Jede übernommene Subskala geht vollständig ein (Regel 10).
- **Bezeichnung:** Theorie bzw. Instrument benennst du je Konstrukt nach der Herkunftsangabe aus C2 (Regel 5), sekundär zitierte Werke als „Primärwerk (Jahr, zit. n. Quelle, Jahr)“. Fehlt die Herkunftsangabe, nennst du das Instrument der Quelle und vermerkst „Herkunft nicht in den Quellen enthalten“.
- **Definition:**
  - Wörtlich aus C1, in Anführungszeichen mit Seite; Auslassungen mit […].
  - Fehlt sie: „Definition nicht in den Quellen enthalten; Operationalisierung: …“ (wörtlich aus C2).
  - Instruktionstexte, Itemformulierungen, Faktorbezeichnungen und Modellannahmen sind keine Definitionen.
- **Sekundärzitate:** nur, wenn C1 bzw. C2 die Zuschreibung im Literaturverzeichnis der Quelle nachweist; Format wie unter „Bezeichnung“. Passt der Titel nicht zum Konstrukt, ordne das Konstrukt der Quelle selbst zu und vermerke die Unstimmigkeit mit [eigene Bewertung].
- **Validierter Umfang:**
  - Verwende nur Konstrukte bzw. Subskalen aus dem finalen Modell der Quelle.
  - Ein Ausschluss aus C4 gilt nur für das dort genannte Konstrukt (Regel 4). Steht dort „Bezug nicht genannt“, wendest du ihn nicht an und führst ihn unter „Offene Punkte“ auf.
  - Ging ein Konstrukt nur als Einzelindikator ein, weise es als „als Skala nicht validiert“ aus.
- **Messverfahren (C3):** Übernimm es vollständig, wenn Items davon abhängen (Filter- oder Häufigkeitsfragen, Szenario, Technologiebeschreibung, Itemstamm). Filteritems kommen mit Antwortformat und Filterregel in Tabelle B. Ist die Filterregel mehrdeutig (z. B. eine Schwelle bei mehreren Items je Bereich), legst du die Verdichtung als [eigene Bewertung] fest.
- **Blockreihenfolge und Blocknummern:**
  - Übernimm die Reihenfolge der Quelle. Kombinierst du Instrumente oder weichst du ab, dokumentiere die Abweichung mit Belegzitat zur Originalreihenfolge (C3) und Begründung [eigene Bewertung].
  - Nummeriere alle Blöcke einmal fortlaufend in dieser Reihenfolge, einschließlich der Technologiebeschreibung, und stelle die Liste Tabelle B voran.
  - Instruktion, Tabelle B, Skalenangaben, Optionshinweise und Auswertungshinweise verwenden ausschließlich diese Nummern.
- **Aggregation:**
  - Bildet die Quelle ein Konstrukt über Teilbereiche (z. B. Mittelwert über alle relevanten Aufgabenarten), übernimm die Aggregation mit **allen** Teilbereichen der Quelle.
  - Eine Teilauswahl ist nur zulässig, wenn ein Belegzitat genau diese Teilauswahl für genau dieses Konstrukt nennt.
  - Prüfe für jedes Einsatzfeld aus den Fall-Parametern, welcher Teilbereich es abdeckt, und dokumentiere die Zuordnung in Tabelle A. Deckt keiner ein Einsatzfeld ab, gilt Regel 9.

##### 2.2 Items
- **Anzahl (Vorrang in dieser Reihenfolge):**
  1. Validierte Skala oder Subskala (Regel 10): alle Items der finalen Fassung. Kürzen nur, wenn ein Belegzitat eine validierte Kurzform genau dieser Skala nennt.
  2. Konstrukt über Teilbereiche (2.1, Aggregation): alle Items aller Teilbereiche.
  3. Sonst (als Skala nicht validiert): 3–4 Originalitems; hat die Quelle weniger, alle. Begründe die Auswahl in „Adaption“.
  4. Kein Konstrukt (auch kein Kriterium) wird mit nur einem Item gemessen, wenn die Quelle mehr enthält.
  5. Redundanz, Begriffsgleichheit mit anderen Konstrukten und eingeschränkte Passung sind keine Gründe, Items wegzulassen.
- **Item-ID:** Lege das Schema einmal fest und stelle es Tabelle B voran:
  - aus dem Katalog: Katalogpräfix + Fragebogen-Nr. + Originalbezeichnung;
  - direkt aus einer Quelle: Quellenpräfix + Originalnummer;
  - ohne Nummer: Präfix + Konstruktname + Position.
- **Originalitem:**
  - zeichengenau aus C2, aus genau einer Quellenversion, mit Fundstelle und Herkunftsangabe;
  - Sprachfassung nach Regel 10: Liegt der Wortlaut in der validierten Sprachfassung vor, ist er der Ausgangspunkt (kein Ü). Als deutsche Fassung gilt nur ein abgedruckter deutscher Wortlaut; der Hinweis, eine Studie sei auf Deutsch erhoben worden, genügt nicht;
  - bei „⚠ Abweichung“: beide Fassungen nennen, Wahl mit [eigene Bewertung] begründen, Pretest-Prüfpunkt angeben. Bevorzuge die Fassung, deren Modus zu Itemstamm und Blockfrage passt.
- **Erlaubte Änderungen (ohne Beleg, aber dokumentiert):** Technologiename, Pronomen/Genus, Modus, Auflösung doppelter Verneinungen. Jede andere Änderung ist I und braucht ein wörtliches Belegzitat zur Definition oder zu einem Parallelitem; ohne Beleg unterbleibt sie (Regel 10).
- **Adaptionscodes:** Ü = Übersetzung, K = Kontext, I = Inhalt, S = Skala/Antwortformat.
  - Dokumentiere jede Änderung am Wortlaut, auch Streichungen und einzelne Wörter. Der Kerninhalt bleibt erhalten (z. B. „ohne Kontrolle“ bei Trust).
  - Ersetze unpassende Inhalte (z. B. Bezugspersonen) nicht durch eigene. Behalte das Item, kennzeichne die eingeschränkte Passung mit [eigene Bewertung] und nenne einen Pretest-Prüfpunkt.
  - Einen Ebenen- oder Perspektivwechsel („wir“ → „ich“) nimmst du nur vor, wenn das Item für die Zielgruppe sonst unbeantwortbar ist (Regel 8) und die Definition aus C1 die Ebene der Zielgruppe ausdrücklich einschließt (Belegzitat). Kennzeichne ihn als I (nicht validiert) und weise jede Hypothese mit diesem Konstrukt als explorativ aus. Ohne diesen Beleg ist das Konstrukt für den Fall nicht verwendbar (Regel 9).
  - „Unverändert“ steht nur, wenn Wortlaut und Antwortformat dem Original entsprechen.
- **Übersetzung (Ü):** Wähle die bedeutungsgleiche Entsprechung, ohne Bedeutungsverengung oder Nebenbedeutung (z. B. „tasks“ = „Aufgaben“, nicht „Aufträge“).
- **Modus:**
  - Absichten, aktuelles Wissen und Einstellungen bleiben im Indikativ.
  - Konjunktiv nur, wo das Item eine Nutzung oder eine dabei entstehende Bewertung bzw. Emotion voraussetzt.
  - Ein Futur im Original bleibt Futur.
  - Innerhalb eines Blocks verwenden Instruktion, Blockfrage und alle Items einer Skala denselben Modus. Bei Mischmodus entscheidet Regel 8; dokumentiere die Abweichung als K.
  - Lässt sich eine vorausgesetzte Erfahrung nicht über den Modus beheben, bleibt der validierte Wortlaut (Rangfolge); nenne einen Pretest-Prüfpunkt.
  - Passt eine Blockfrage nicht zum Antwortformat (z. B. „Wie gut …?“ bei Zustimmungsskala), setze sie als Überschrift ohne Frageform und dokumentiere das als K.
- **Allgemeine Instrumente:** Für „KI allgemein“ validierte Items bleiben allgemein. Eine Verengung auf die Fall-Technologie ist eine Abweichung und unterbleibt ohne wörtlichen Beleg (Regel 10).
- **Eindimensionalität und Wortwahl:**
  - Füge keine Begriffe, Gegenstände, Bedingungen, Abschwächer oder Verstärker hinzu.
  - Löse doppelte Verneinungen und mehrdeutige Negationen auf, ohne die Intensität zu verändern (nicht „keine Bedenken“ → „ich bin sicher“). Kennzeichne das als I.
  - Kommt die bedeutungsgleiche Entsprechung bei Ü oder K bereits in Items eines anderen Konstrukts vor, wähle ein anderes Wort nur, wenn es ebenfalls bedeutungsgleich ist. Sonst behalte sie und nenne einen Pretest-Prüfpunkt. Begriffsgleichheit rechtfertigt weder eine Bedeutungsverschiebung noch das Weglassen eines Items.
  - Begriffspaare, Beispielaufzählungen, Verstärker, gekoppelte Bedingungen oder Maße (z. B. „meist gut“), Präsuppositionen in Nebensätzen (z. B. „trotz …“, „obwohl …“) und mehrdeutige Begriffe aus dem Original bleiben erhalten. Prüffrage: Nennt C4 für die Skala dieses Items einen Kennwert oder eine Validierungsaussage? Ja → Kennwert bzw. Aussage mit Seite in „Adaption“ zitieren. Nein (auch bei Einzelindikatoren) → inhaltliches Belegzitat + Pretest-Prüfpunkt. Bei Mehrdeutigkeit immer ein Pretest-Prüfpunkt.
  - Ausnahme: Steht ein Verstärker oder Zusatz nur in einer von zwei Parallelfassungen (z. B. Filter- und Fit-Item zum selben Inhalt) und nennt C4 keinen Itemkennwert, gleiche die Fassung ohne Verstärker an (I, Belegzitat: Parallelitem).
  - Weichen Parallelfassungen inhaltlich ab (nicht nur durch einen Verstärker), bleiben beide Wortlaute; markiere „⚠ Abweichung“ und nenne einen Pretest-Prüfpunkt.
- **Polung (R):**
  - Nur, wenn die Quelle die Umpolung belegt oder das Item der Konstruktrichtung inhaltlich widerspricht. Ohne Beleg: [eigene Bewertung], auch bei jeder Hypothese mit diesen Items.
  - Items eines eigenständigen Faktors (z. B. Fear) sind innerhalb ihrer Skala nicht invers.
  - Sind alle Items einer Skala gleich gepolt, bleibt der Wortlaut. Begründe das mit dem Kennwert der Validierung (Seite) oder mit „als Skala nicht validiert“; Zustimmungstendenz wird Pretest-Prüfpunkt.

##### 2.3 Hypothesen
- Nur Hypothesen aus C5, die die Quelle empirisch geprüft hat.
- Jede Hypothese verbindet genau ein Prädiktor- mit genau einem Kriteriumskonstrukt. Ein Prädiktor darf in mehreren Hypothesen vorkommen, wenn die Quelle jede dieser Beziehungen geprüft hat. „KI-Readiness“ ist weder Prädiktor noch Kriterium, da kein Gesamtwert gebildet wird.
- Vergleiche die Herkunft von Prädiktor und Kriterium (C5). Nimm die Hypothese nur bei gleicher Theorie auf (Regel 11).
- Prädiktor und Kriterium stammen aus derselben Quelle und werden nach 2.2 gemessen (mindestens 3 Items bzw. alle). Fehlt das Kriterium, nimm seine Items auf oder lass die Hypothese weg.
- **Überschneidung:** Prüfe, ob sich Prädiktor- und Kriteriumsitems inhaltlich überschneiden (z. B. gleicher Itemstamm, bedeutungsnahe Aussagen) oder sich in der Spezifität unterscheiden (allgemein vs. konkretes System). Vermerke den Befund in Tabelle C mit einem Diskriminanzkennwert aus C4 (z. B. HTMT) oder einem Pretest-Prüfpunkt.
- Nenne H-Nr., Seite, Ergebnis (bestätigt / nicht bestätigt) und das wörtliche Belegzitat.
- Vermerke, wenn das Ergebnis aus einem Modell mit weiteren, hier nicht erhobenen Prädiktoren stammt oder ein Konstrukt anders gebildet wird als in der Quelle.
- **Explorativ** ist eine Hypothese, wenn ein Konstrukt anders gebildet wird als in der Quelle, einen Ebenenwechsel enthält (2.2) oder auf einer nicht validierten Übersetzung beruht (Regel 10).
- Verwende den Konstruktnamen aus Tabelle A.
- Gegenannahme nur mit empirischem Beleg der Quelle (Zitat, Seite). Verallgemeinere sie nicht über die untersuchten Gruppen oder Bedingungen hinaus. Ohne Beleg: [eigene Bewertung].

##### 2.4 Instruktion
- Anonymitätshinweis, vor dem ersten technologiebezogenen Item.
- **Technologiebeschreibung** [Modellwissen]:
  - Übernimm Gliederung und Umfang der Beschreibung aus C3 (z. B. Teilabschnitte), wenn die Quelle eine vorgibt;
  - Inhalt: höchstens die Einsatzfelder aus den Fall-Parametern;
  - kein Begriff, der in Items, Itemstämmen oder Aufgabenbeschreibungen eines Teilbereichs vorkommt (z. B. „planen“ bei Planungsaufgaben); lässt sich ein Einsatzfeld nur so benennen, lass es weg;
  - Funktionen mit Modalverben („kann …“);
  - kein Nutzerverhalten und keine Kontrollpraxis als gegeben (kein „Ergebnisse werden geprüft“);
  - keine Vorteile, keine Wertungen.
  - Bleibt die Beschreibung hinter der Quelle zurück (Umfang, Abbildungen, nicht übernommene Technologiemerkmale) oder fehlen Einsatzfelder, führe das unter „Offene Punkte“ als Einschränkung der Urteilsbasis auf.
- Gibt die Quelle ein Szenario, einen Itemstamm oder einen Instruktionstext vor, übernimm ihn an der entsprechenden Stelle. Für übernommene Texte gelten dieselben Änderungsregeln und Adaptionscodes wie für Items (2.2); dokumentiere jede Änderung über den Technologienamen hinaus einzeln.
- Die Instruktion nennt keine Filterregeln, Hypothesen oder Auswertungslogik.
- Hinweise auf Antwortoptionen (z. B. „kann ich nicht beurteilen“) gelten nur für die Blöcke, die diese Option haben; benenne diese Blöcke mit den Nummern aus 2.1.

##### 2.5 Skala
- **Validierte Skala (Regel 10):** Originalskala aus C3 unverändert (Stufenzahl, Anker, Urteilstyp), ohne Zusatzoption, außer die Quelle enthält sie.
  - Eine Umstellung, ein anderer Urteilstyp (z. B. Fähigkeitseinschätzung → Zustimmung) oder eine Zusatzoption ist nur zulässig, wenn ein Zitat genau diese Änderung ausdrücklich für geeignet erklärt. Ein Hinweis, andere Skalierungen „zu prüfen“, genügt nicht. Dann: jedes betroffene Item als S, Originalskala, Seite und Grund in Tabelle A, als nicht validiert ausweisen.
  - Liegen die Anker nicht in der Fragebogensprache vor, übersetze nur die Anker wörtlich (Ü, nicht validiert) und führe das unter „Offene Punkte“ auf.
- **Nicht validierte Skala mit Originalskala in C3:** Originalskala behalten.
- **Originalskala nicht in den Quellen enthalten:** Standard 1–5 (stimme überhaupt nicht zu … stimme voll zu) + „kann ich nicht beurteilen“ (= fehlender Wert); als S mit [eigene Bewertung] kennzeichnen.
- Eine Zusatzoption entfällt, wenn ein übernommener Instruktionstext zur Antwort ohne Erfahrung auffordert (z. B. „auch wenn Sie … noch nicht gearbeitet haben“).
- **Filter- und Häufigkeitsfragen** behalten ihr Originalformat.

##### 2.6 Auswertung
- Jede Skala getrennt; keine Skalen verschiedener Faktoren oder Quellen zusammenfassen. KI-Readiness wird als Profil der Skalenwerte je Dimension berichtet, nicht als Gesamtwert.
- Aggregationsregel je Skala mit Belegzitat aus C4 genau dieses Instruments (Regel 4); ohne Beleg: [eigene Bewertung].
- Kennwerte nur für die Fassung berichten, für die die Quelle sie angibt (Skala und Itemzahl).
- Filter- und Aggregationsregeln aus 2.1, Invertierung aller (R)-Items und die Behandlung von „kann ich nicht beurteilen“ (falls vorhanden) mit Blocknummern.

---

#### Typische Fehler (nicht wiederholen)
- ✗ Ausschluss von Indikatoren eines Prädiktors (TC) als Begründung für gekürzte Fit-Items (TTF) verwendet.
- ✗ „Die Autor:innen empfehlen, andere Skalierungen zu prüfen“ als Begründung für 5 statt 11 Stufen.
- ✗ Instruktion: „nur für Aufgabenarten, die Sie mindestens monatlich ausführen“.
- ✗ Technologiebeschreibung: „Die Ergebnisse werden von den Nutzer:innen geprüft“.
- ✗ Technologiebeschreibung mit Begriffen der Aufgabenarten („Abläufe planen“, „Daten auswerten“), die TTF-Urteile für diese Aufgabenarten anheben können.
- ✗ Faktor „Acceptance“ umbenannt in „Vertrauen und Nutzenerwartung“.
- ✗ Heftnummer bzw. Autor:innen aus Vorwissen ergänzt oder weggelassen.
- ✗ Tabelle D „erfüllt“, obwohl Tabelle B oder „Offene Punkte“ eine Abweichung dokumentieren.
- ✗ Itemzahl geschätzt statt gezählt.
- ✗ BI dem TTF-Modell zugeordnet, obwohl die Quelle „adapted from UTAUT“ angibt.
- ✗ Theorieübergreifende Hypothese (TTF → BI aus UTAUT) übernommen, weil die Quelle sie geprüft hat.
- ✗ Instruktion und Blockfrage im Konjunktiv („könnte“), Items im Indikativ („kann“).
- ✗ „Strikt“ im Fit-Item beibehalten, obwohl das parallele Filteritem es nicht enthält und keine Itemkennwerte vorliegen.
- ✗ Copilot in zwei Sätzen beschrieben, obwohl die Quelle eine gegliederte Beschreibung mit Abbildungen vorgibt, ohne Vermerk unter „Offene Punkte“.
- ✗ Blockreihenfolge der Quelle (Produktitems vor ATAI) umgestellt, ohne die Abweichung zu dokumentieren.
- ✗ Blocknummern in Blockreihenfolge, Skalenangaben und Instruktion unterschiedlich vergeben.
- ✗ „Kopie“-Dateien als nicht ausgewertet geführt, obwohl nur sie vorlagen.
- ✗ Kompetenzinstrument (MAILS) verworfen, weil es „keine Akzeptanz misst“, obwohl es eine Readiness-Dimension abdeckt.
- ✗ Validierte Subskalen (MAILS Use & Apply, Know & Understand) auf 4 von 6 Items gekürzt und α der 6-Item-Fassung berichtet.
- ✗ Modularitätszitat (Subskalen getrennt einsetzbar) als Beleg für eine Itemauswahl innerhalb einer Subskala verwendet.
- ✗ Items gestrichen oder sinnverschiebend übersetzt („tasks“ → „Aufträge“), nur um Wortgleichheit mit anderen Konstrukten zu vermeiden.
- ✗ Eigene Übersetzung eingesetzt, obwohl die Skala auf Deutsch validiert wurde und nur der deutsche Wortlaut im Inventar fehlte.
- ✗ Zusatzoption „kann ich nicht beurteilen“ ohne Quellenbeleg ergänzt, im Widerspruch zur übernommenen Instruktion „auch wenn Sie … noch nicht gearbeitet haben“.
- ✗ „Keine Itemkennwerte“ angegeben, obwohl die Quelle eine Validierungsaussage zu allen Items enthält („all items loaded significantly“).
- ✗ Mittelwertregel eines Instruments als Beleg für die Auswertung aller Skalen verwendet.
- ✗ Instruktionstext über den Technologienamen hinaus geändert („einsetzen würden“ → „beabsichtigen“), nur als K gekennzeichnet.
- ✗ Sekundärzitat umgekehrt notiert („zit. n. Long & Magerko (2020)“ statt „Long & Magerko (2020, zit. n. Carolus et al., 2023)“).
- ✗ Herkunft eines Konstrukts in Teil I und Teil II unterschiedlich angegeben.
- ✗ Gesamtwert „KI-Readiness“ aus Skalen verschiedener Instrumente gebildet.
- ✗ Eine eigene Definition von KI-Readiness formuliert.

---

#### Selbstkontrolle vor der Ausgabe
Prüfe jede Zeile von Tabelle A–C, die Instruktion und die Auswertungshinweise am Inventar, nicht aus dem Gedächtnis, und korrigiere Verstöße gegen die Regeln dieses Prompts. Gib kein Prüfprotokoll aus. Die Prüfung und Tabelle D entstehen im Prüfprompt (neuer Chat).

---

#### Ausgabe
**Teil I – Inventar (Schritt 1)**
1. 1a Formatanalyse
2. 1b Auswahl
3. 1c Vollinventar (C1–C5 je ausgewählter Quelle)
4. Liste aller ⚠-Markierungen

**Teil II – Fragebogen (Schritt 2)**
1. **Instruktion** (Anonymitätshinweis, neutrale Technologiebeschreibung; Blocknummern aus 2.1)
2. **Tabelle A – Auswahl:** Readiness-Dimension | Theorie/Instrument (Herkunft laut Quelle) | Konstrukt (Originalname) | Definition laut Quelle (Seite) | Quelle | Originalskala (Seite) | validiert (ja: Kennwert mit Seite / nein) | Passung zum Fall (inkl. Zuordnung der Einsatzfelder) | Belegzitat (wörtlich, Seite) | verworfene Alternativen
3. **Tabelle B – Fragebogen** (gruppiert nach Dimension und Theorie; ID-Schema und nummerierte Blockreihenfolge davor): Block | Item-ID | Konstrukt | Originalitem (Fundstelle) | finales Item | Antwortformat | Adaption (Code + Begründung) | (R)
4. **Tabelle C – Hypothesen:** H | Hypothese | Gegenannahme | Prädiktor-Items | Kriterium-Items | Herkunft Prädiktor / Kriterium | Überschneidung und Spezifität (Befund + Kennwert oder Pretest-Prüfpunkt) | Quelle (H-Nr., Seite, Ergebnis) | Belegzitat (wörtlich) | explorativ (ja/nein + Grund)
5. **Auswertungshinweise** (nach 2.6)
6. **Offene Punkte** (nicht erfüllbare Vorgaben, nicht aufgenommene Hypothesen und Einschränkungen mit Grund; „keine“, wenn leer)
7. **Literaturverzeichnis nach APA 7:** alle direkt zitierten Quellen, auch die verworfenen, ausschließlich mit Angaben aus 1a. Sekundär zitierte Werke nur im Text.

Weitere Abschnitte (z. B. Pretest-Prüfpunkte) nur, wenn jede Aussage belegt oder gekennzeichnet ist und den Tabellen nicht widerspricht.

**Formatregeln:** Tabellen mit genau den genannten Spalten; eine Zeile je Datensatz, Item bzw. Hypothese; keine zusammengefassten Zellen; Item-IDs in allen Tabellen identisch geschrieben; leere Werte als „nicht in den Quellen enthalten“.

**Portionierung:** Gib zuerst Teil I aus, danach Teil II. Beende eine Antwort nur nach einer vollständigen Tabelle mit „Fortsetzung folgt – bitte ‚weiter‘ eingeben“. Setze nach „weiter“ genau dort fort, ohne Inhalte zu wiederholen oder zu ändern.

## Anhang F – Prüfprompt V8.2 (Projektfassung)

*Projektfassung, in allen Läufen verwendet. Die Repo-Fassung weicht nur in Zeile 3 und Input 2 ab („V8.2“ statt „V8“).*

### Prompt V8.2 – Prüfprompt: Quelleninventar und Fragebogen (KI-Readiness)

Dieser Prompt prüft das Ergebnis des Erstellungsprompts V8. Verwende ihn in einem neuen Chat ohne Verlauf aus der Erstellung, damit Begründungen des Entwurfs nicht in die Prüfung einfließen.

#### Input
1. **Originalquellen** (Paper, Itemkataloge, Itemblätter) = Referenz für Teil I (Inventar)
2. **Erstellungsprompt V8** = Regelwerk und Prüfmaßstab (Fall-Parameter, Goldene Regeln 1–11, Abschnitte 1a–1c und 2.1–2.6, Typische Fehler, Ausgabeformat)
3. **Entwurf** (Teil I und Teil II) = zu prüfendes Ergebnis. Teil I wird zuerst gegen die Originalquellen geprüft; mit den Korrekturen aus deiner Fehlerliste ist er danach die Referenz für Teil II.
4. **Durchlauf-Nr.:** [1 / 2 / 3 – vom Menschen eintragen]
5. **Fehlerlisten früherer Durchläufe:** [vom Menschen einfügen oder „keine“]

Andere Dokumente (frühere Fragebögen, Gutachten, ältere Prompts) ignorierst du.

#### Rolle
Du bist unabhängige Prüferin und hast den Entwurf nicht erstellt. Du prüfst Teil I nur gegen die Originalquellen und Teil II nur gegen das geprüfte Inventar (Teil I). Maßstab sind die Regeln des Erstellungsprompts. Du prüfst nie gegen deine Erinnerung oder gegen Begründungen im Entwurf. Jede Angabe gilt als falsch, bis du sie an der Fundstelle bestätigt hast. Einen neuen Fragebogen erstellst du nicht.

#### Grundsätze
- „Nicht in den Quellen enthalten“ ist eine geprüfte Feststellung, wenn du die ganze Quelle durchsucht hast.
- „⚠ Abweichung“ ist eine geprüfte Tatsache über die Dokumente und bleibt stehen.
- Erfinde keine Mängel. Ist ein Punkt regelkonform, gibt es keinen Befund.
- Bewertungen ohne Quellenbeleg kennzeichnest du mit [eigene Bewertung].

#### Vorgehen
1. **Teil I zuerst.** Gehe jede Zeile von 1a, 1b, 1c und der ⚠-Liste einzeln durch.
   - Schlage jede Angabe an der Fundstelle nach und vergleiche zeichen- bzw. zahlengenau.
   - Durchsuche jede ausgewählte Quelle erneut nach fehlenden Datensätzen (Items, Definitionen, Kennwerte, Validierungsaussagen, Hypothesen, Erhebungssprache).
   - Löse jedes „⚠ nicht geprüft“ auf: bestätigen oder korrigieren.
2. **Teil II erst danach,** gegen das geprüfte Inventar. Gehe jede Zeile einzeln durch: Instruktion, Tabellen A–C, Auswertungshinweise, Offene Punkte, Literaturverzeichnis.
3. Prüfe jede Zeile gegen jeden Punkt der Prüftabelle und gegen die Liste „Typische Fehler“ des Erstellungsprompts.
4. Zähle die Zeilen von Tabelle B neu. Vergleiche Itemzahlen, Item-IDs und Blocknummern über alle Abschnitte.
5. Prüfe jeden Korrekturvorschlag erneut gegen die Prüftabelle, bevor du ihn ausgibst.

#### Prüftabelle

**Teil I – Inventar (Referenz: Originalquellen)**

| Nr. | Prüfpunkt | Regel/Abschnitt |
|---|---|---|
| I-1 | Jedes Zitat zeichengenau an der Fundstelle bestätigt; Seitenangabe als gedruckte Seite oder „PDF-S.“; keine geschätzte Seite | 1 |
| I-2 | Bibliografie nur aus Titelseite, Kopf- oder Fußzeile; nichts aus Vorwissen; fehlende Angaben als „nicht in den Quellen enthalten“ | 2 |
| I-3 | Dateianzahl gezählt; Kopie-Regel angewendet; Bestandsspalten in 1a („ja (Fundstelle)“ / „nein“) korrekt | 1a |
| I-4 | Auswahl: Formatkriterium angewendet; Dimensionen aus den Konstrukten der Quellen abgeleitet und als [eigene Bewertung] gekennzeichnet; je Dimension genau eine Quelle oder „keine passende Quelle“; jede Entscheidung mit wörtlichem Belegzitat | 1b, 3, 5, 9 |
| I-5 | C1: Definition und Operationalisierung getrennt; Sekundärzitate im Format „Primärwerk (Jahr, zit. n. Quelle, Jahr)“ und im Literaturverzeichnis der Quelle nachgewiesen | 1c |
| I-6 | C2: alle Items vollständig, in allen vorhandenen Sprachfassungen; Herkunftsangabe wörtlich oder „nicht in den Quellen enthalten“ | 1c, 5 |
| I-7 | C3: Antwortskala mit Ankern wörtlich; Instruktions- und Blockfragetexte wörtlich; Filterregel; Blockreihenfolge; Erhebungssprache | 1c |
| I-8 | C4: Ausschlüsse mit Bezug; Kennwerte mit Bezug auf Skala und Itemzahl; Validierungsaussagen und Diskriminanzkennwerte nicht übersehen | 1c, 4 |
| I-9 | C5: Hypothesen wörtlich; Herkunft von Prädiktor und Kriterium aus C2; Ergebnis mit Kennwerten; weitere Prädiktoren | 1c |
| I-10 | Abweichungen zwischen Fassungen markiert und nicht aufgelöst; kein Datensatz fehlt; kein „⚠ nicht geprüft“ mehr vorhanden | 1c |

**Teil II – Fragebogen (Referenz: geprüftes Inventar)**

| Nr. | Prüfpunkt | Regel/Abschnitt |
|---|---|---|
| II-1 | Jede Angabe stammt aus dem Inventar; keine Fakten aus Vorwissen | 1, 2 |
| II-2 | Jede Entscheidung hat ein wörtliches, tragendes Belegzitat, das das betroffene Konstrukt und die betroffene Ebene ausdrücklich nennt | 3, 4 |
| II-3 | Eine Theorie je Konstrukt laut Herkunftsangabe (C2); Name nach Regel 6; Bezugsebene unverändert oder durch die Definition gedeckt und als I gekennzeichnet | 5–7, 2.2 |
| II-4 | Dimensionen wie in 1b; keine eigene Definition von KI-Readiness; jede Dimension durch genau eine Quelle abgedeckt oder unter „Offene Punkte“; Subskalen-Teilauswahl belegt; Auswertung als Profil ohne Gesamtwert | 1b, 2.1, 2.6 |
| II-5 | Validierte Skalen vollständig, im Originalformat, ohne Zusatzoption und in der validierten Sprachfassung; jede Abweichung mit wörtlichem Beleg, sonst unterlassen; fehlende Sprachfassung unter „Offene Punkte“ | 10, 2.2, 2.5 |
| II-6 | Itemzahl je Konstrukt nach der Vorrangfolge in 2.2; Filteritems, Filterregel und Aggregation mit allen Teilbereichen; jedes Einsatzfeld zugeordnet oder unter „Offene Punkte“; Blockreihenfolge wie Quelle oder Abweichung dokumentiert | 2.1, 2.2, 9 |
| II-7 | Items nicht zweidimensional, suggestiv oder mehrdeutig verneint; Begriffspaare, gekoppelte Maße, Verstärker und Präsuppositionen nur mit Kennwert bzw. Beleg; Parallelfassungen angeglichen oder als Abweichung markiert; keine vorausgesetzte Erfahrung oder Entscheidungsbefugnis; Modus je Block einheitlich (Instruktion, Blockfrage, Items) | 8, 2.2 |
| II-8 | Nur erlaubte Änderungen oder I mit wörtlichem Belegzitat; keine Intensitätsänderung; Übersetzungen bedeutungsgleich; kein Item wegen Begriffsgleichheit gestrichen oder umgedeutet; jede Ü/K/I/S-Änderung dokumentiert, auch in übernommenen Instruktionstexten | 2.2, 2.4 |
| II-9 | Instruktion: Anonymitätshinweis; Beschreibung mit Gliederung der Quelle, Modalverben, ohne Praxis, Vorteile und ohne Begriffe aus Items oder Aufgabenbeschreibungen; Einschränkungen der Urteilsbasis unter „Offene Punkte“; keine Filterregeln, Hypothesen, Auswertungslogik; Optionshinweise mit den richtigen Blocknummern | 2.4 |
| II-10 | Skala nach 2.5; jede Änderung belegt und als nicht validiert ausgewiesen; keine Zusatzoption im Widerspruch zu einer übernommenen Instruktion | 2.5 |
| II-11 | Hypothesen: Prädiktor und Kriterium aus derselben Theorie, sonst unter „Offene Punkte“; je Hypothese ein Prädiktor und ein Kriterium; beide gemessen; Überschneidung und Spezifität geprüft; Belegzitat; Modellabweichungen vermerkt; Gegenannahme belegt oder gekennzeichnet; explorative Hypothesen markiert | 11, 2.3 |
| II-12 | Auswertung: Aggregationsregel je Skala aus derselben Quelle belegt oder gekennzeichnet; Kennwerte nur für die passende Fassung; jedes (R)-Item genannt; Filter- und Aggregationsregel enthalten | 2.6 |
| II-13 | Konsistenz: Itemzahlen durch Zählen der Zeilen von Tabelle B; jede Item-ID aus Tabelle C existiert in Tabelle B; Blocknummern in allen Abschnitten identisch; Teil I und Teil II widerspruchsfrei (z. B. Herkunft, Kennwerte); keine Pauschalaussagen (z. B. „vollständig validiert“) | Konsistenz |
| II-14 | Literatur nur aus 1a; vollständige Autorenliste; im Text ab drei Autor:innen „et al.“; Sekundärquellen (auch Herkunft der Items) im Text als „Primärwerk (Jahr, zit. n. Quelle, Jahr)“; fehlende Angaben als „nicht in den Quellen enthalten“ | 1, 2 |

#### Ausgabe

**Schritt 1 – Fehlerliste**
Nr. | Teil | Abschnitt/Tabelle | Zeile bzw. Item-ID bzw. H | Prüfpunkt (I-n / II-n) | Befund | korrekte Angabe | Fundstelle (Quelle bzw. Inventar)

Danach **Protokoll:** Durchlauf-Nr. | geprüfte Zeilen Teil I (gezählt) | geprüfte Zeilen Teil II (gezählt) | Fehler Teil I | Fehler Teil II | fehlende Datensätze

Enthält die Fehlerliste keine Einträge, schreibe: „Durchlauf [Nr.]: 0 Fehler – Inventar und Fragebogen freigegeben.“ Gib danach Tabelle D aus.

**Schritt 2 – nur nach Eingabe „korrigieren“**
- Gib die vollständige korrigierte Fassung von Teil I und Teil II aus (Ausgabeformat des Erstellungsprompts, ohne Tabelle D).
- Ziehe alle Folgeänderungen nach: Inventar, andere Tabellen, Item-IDs, Itemzahlen, Blocknummern, Hypothesen, Auswertung, Literatur. Übernimm bestätigte Zeilen unverändert.
- **Im Durchlauf 3:** Was nicht bestätigt werden kann, entfernst du (Regel 9), ziehst die Folgeänderungen nach und führst es unter „Offene Punkte“ auf. Gib danach Tabelle D aus.
- Die korrigierte Fassung ersetzt den Entwurf. Den nächsten Durchlauf startet der Mensch in einem neuen Chat.

**Tabelle D – Prüfprotokoll** (nur bei 0 Fehlern oder nach Durchlauf 3)
Prüfpunkt (I-1 bis II-14) | Status | Nachweis | betroffene Item-IDs bzw. H
- **„erfüllt“** nur mit Nachweis (Belegzitat oder Item-ID). Außerdem dürfen weder Tabelle A–C noch „Offene Punkte“ zu diesem Prüfpunkt eine Abweichung oder Einschränkung nennen.
- **„korrigiert“** mit Angabe, was in einem früheren Durchlauf geändert wurde (laut eingefügten Fehlerlisten).
- **„Abweichung dokumentiert“** bei bewusster, belegter Abweichung von der Quelle.
- **„entfernt“**, wenn ein Element nach drei Durchläufen nicht bestätigt werden konnte.
- **„nicht prüfbar“**, wenn kein Nachweis möglich ist.

**Abschluss** (mit Tabelle D)
1. **Protokoll der Prüfschleifen:** Durchlauf | Fehler Teil I | Fehler Teil II | korrigiert
2. **Offene Punkte:** Element | Grund; „keine“, wenn leer

**Formatregeln:** Tabellen mit genau den genannten Spalten; eine Zeile je Befund; keine zusammengefassten Zellen.

**Portionierung:** Beende eine Antwort nur nach einer vollständigen Tabelle mit „Fortsetzung folgt – bitte ‚weiter‘ eingeben“. Setze nach „weiter“ genau dort fort, ohne Inhalte zu wiederholen oder zu ändern.

