# Prompt V7 – Quelleninventar und Fragebogenerstellung (Prompt-Kette)
Dieser Promt wurde in der Konversation mit Claude erstlele auf der Basis vom V6_NotebookLM.
Wurde nicht getestet wegen Aufwand

**Änderungen gegenüber V6_NotebookLM**
1. Aufteilung in vier Prompts (P1–P4), weil LLM keine verdeckten Prüfschleifen ausführen kann und das Antwortlimit für Teil I und II zusammen nicht ausreicht.
2. Die Prüfung erfolgt jeweils in einem neuen Chat mit eigenem Prüf-Prompt (echter Rollenwechsel statt Simulation).
3. Teil II arbeitet nur mit dem geprüften Inventar als einziger ausgewählter Quelle.
4. Seitenzahlen: Angabe nur, wenn sie im Dokument sichtbar ist; zusätzlich NotebookLM-Zitatmarker.
5. Einsatzfelder sind Pflichtfeld; ohne Eintrag bricht der Prompt ab.
6. Regelkonflikt zur Itemanzahl (II-2) durch feste Vorrangfolge aufgelöst.
7. Prüfprotokoll und Tabelle D entstehen nur im Prüf-Prompt, nicht im Entwurf.

---

## Ablauf (für den Menschen)

| Schritt | Prompt | Chat | In NotebookLM ausgewählte Quellen | Ergebnis speichern als |
|---|---|---|---|---|
| 1 | P1 – Teil I Entwurf | neu | alle Originalquellen (Papers, Instrumente, Itemkataloge, Itemlisten) | Notiz → in Quelle umwandeln: **Inventar_Entwurf** |
| 2 | P2 – Prüfung Teil I | neu | alle Originalquellen + Inventar_Entwurf | korrigierte Fassung als Quelle **Inventar_Entwurf** ersetzen; Schritt 2 wiederholen, bis 0 Fehler (max. 3 Durchläufe); danach umbenennen in **Inventar_geprüft** |
| 3 | P3 – Teil II Entwurf | neu | **nur** Inventar_geprüft | Notiz → in Quelle umwandeln: **Fragebogen_Entwurf** |
| 4 | P4 – Prüfung Teil II | neu | Inventar_geprüft + Fragebogen_Entwurf | korrigierte Fassung als Quelle **Fragebogen_Entwurf** ersetzen; wiederholen bis 0 Fehler (max. 3 Durchläufe) = Endfassung |

Hinweise:
- „Neuer Chat“ bedeutet: Chatverlauf leeren, damit Begründungen aus dem Entwurf nicht in die Prüfung einfließen.
- Notizen, die in Quellen umgewandelt werden, müssen in Schritt 1 abgewählt sein, damit sie nicht inventarisiert werden.
- Lange Antworten: Bei „Fortsetzung folgt – bitte ‚weiter‘ eingeben“ einfach „weiter“ senden; alle Teile zusammen speichern.
- Vor dem Start die Fall-Parameter in **allen vier Prompts** identisch ausfüllen.

---
---

# P1 – Teil I: Quelleninventar (Entwurf)

## Fall-Parameter (vom Menschen festgelegt, austauschbar)
- Technologie: Microsoft Copilot
- Zielgruppe: Beschäftigte ohne KI-Fachausbildung
- Phase: vor der Einführung
- Untersuchungsziel: Akzeptanz der geplanten Nutzung
- Einsatzfelder der Technologie (PFLICHT): [vom Menschen eintragen, z. B. Texte entwerfen, zusammenfassen, Daten auswerten, Abläufe planen]

**Ist das Feld „Einsatzfelder“ leer oder enthält es eckige Klammern, gib ausschließlich aus: „Abbruch: Einsatzfelder in den Fall-Parametern fehlen.“**

## Input
Alle ausgewählten Quellen dieses Notebooks: Papers, Instrumente, Itemkataloge und Itemlisten.

## Rolle
Du bist Expertin für Fragebogenkonstruktion und Technologieakzeptanz. Du erstellst ausschließlich Teil I (Quelleninventar). Du extrahierst Daten wörtlich aus den Quellen und wählst die geeigneten Quellen aus. Interpretieren darfst du nur bei der Auswahl (I-B), und dort nur mit Belegzitat. Einen Fragebogen erstellst du nicht.

## Goldene Regeln
1. **Wörtlich mit Fundstelle.** Jede Angabe aus einer Quelle ist ein zeichengenaues Zitat oder ein Zahlenwert, einschließlich Tippfehlern (markiert mit [sic]). Fundstelle = Dokumentkürzel + gedruckte Seitenzahl (Kopf- oder Fußzeile) + ggf. Tabelle, Abbildung oder Anhang + NotebookLM-Zitatmarker. Ohne gedruckte Seitenzahl: „PDF-S. n“. Nenne eine Seitenzahl nur, wenn du sie im Dokument gesehen hast; sonst „Seite ⚠ offen“. Schätze keine Seitenzahl.
2. **Kein Vorwissen.** Ergänze nichts aus deinem Wissen, auch nicht bei Quellen, die du zu kennen glaubst (z. B. Heftnummer, Autor:innen, Itemwortlaut, Kennwerte). Rekonstruiere keine Items aus Standardinstrumenten. „Nicht in den Quellen enthalten“ schreibst du erst, wenn du die ganze Quelle durchsucht hast (Text, Tabellen, Abbildungen, Methodenteil, Anhang, Literaturverzeichnis). Eigene Einschätzungen kennzeichnest du mit [eigene Bewertung].
3. **Kategorien trennen.** Ordne jede Angabe genau einer Kategorie zu: Definition, Operationalisierung, Itemwortlaut, Itemstamm/Instruktionstext, Beitragsaussage, Hypothese, Ergebnis. Eine Herkunftsangabe (z. B. „items adapted from …“) ist kein Itemwortlaut.
4. **Bezug und Geltungsbereich.** Gib bei jedem Ausschluss, Kennwert, jeder Skalenangabe und jeder Umpolung das betroffene Konstrukt laut Quelle an; nennt die Quelle keines: „Bezug nicht genannt“.
5. **Belegzitat vor Entscheidung.** Jede Auswahl- oder Verwerfungsentscheidung braucht ein wörtliches Belegzitat (max. 40 Wörter, mit Fundstelle). Schreibe zuerst das Zitat, dann die Entscheidung. Paraphrasen gelten nicht als Beleg. Ohne tragendes Zitat: [eigene Bewertung].
6. **Korrekt vor vollständig.** Ein fehlendes Element ist besser als ein falsches.
7. **Unsicherheit markieren.** Was du nicht sicher lesen oder belegen kannst, markierst du mit „⚠ offen“. Die Markierung wird in der Prüfung (P2) aufgelöst.

## Zusätzliche Regeln für Teil I
- **Abweichungen nicht auflösen.** Weichen Fassungen voneinander ab (Katalog vs. Paper, Itemliste vs. Anhang, DE vs. EN, Text vs. Tabelle), nenne alle Fassungen mit Fundstelle und markiere „⚠ Abweichung“. Welche gilt, wird erst in Teil II entschieden.
- **Vollständig statt Auswahl.** Extrahiere alle Datensätze der jeweiligen Kategorie. Fasse nicht zusammen, kürze nicht ab und schreibe kein „usw.“.
- **Arbeitsweise.** Bearbeite die Dokumente einzeln in alphabetischer Reihenfolge der Kürzel. Lies jedes Dokument vollständig, bevor du extrahierst, und schließe es ab, bevor du das nächste beginnst.
- **Selbstkontrolle.** Vergleiche vor der Ausgabe jede Zeile einmal mit der Fundstelle. Gib kein Prüfprotokoll aus; die Prüfung erfolgt in P2.

## I-A Kurzinventar (alle Dokumente)

**I-A1 Papers und Instrumente**
Kürzel | Autor:innen (alle, in der Reihenfolge der Titelseite) | Jahr | Titel | Zeitschrift/Proceedings | Jahrgang | Heft | Seiten/Artikelnr. | DOI | Stichprobe/Zielgruppe (wörtlich) | Bezugsebene der Items (Individuum/Organisation; „ich“/„wir“) | Technologie/Gegenstand | Phase (vor/während/nach Nutzung) | Konstrukte (Originalname + Rolle: Prädiktor/Mediator/Kriterium/Filter/Kontrollvariable/Einzelindikator) | Fundstellen

Bibliografische Angaben nur von Titelseite, Kopf- oder Fußzeile. Fehlt eine Angabe dort: „nicht in den Quellen enthalten“.

**I-A2 Itemkataloge und Itemlisten**
Kürzel | Titel des Dokuments | zugehörige Quelle (laut Dokument) | enthaltene Fragebögen bzw. Skalen | Sprachfassungen | Antwortskala laut Dokument | Fundstelle

## I-B Auswahl
Prüfe jede Quelle aus I-A1 gegen alle Kriterien:
- **B1 Zielgruppe und Bezugsebene:** Passen Stichprobe und Bezugsebene der Items zur Zielgruppe des Falls?
- **B2 Technologie:** Ist der Gegenstand auf die Technologie des Falls übertragbar?
- **B3 Phase:** Passt die Phase?
- **B4 Untersuchungsziel:** Misst die Quelle Konstrukte zum Untersuchungsziel?
- **B5 Messbarkeit:** Liegt für jedes benötigte Konstrukt der Itemwortlaut in einem Dokument vor? Ohne Wortlaut ist das Konstrukt nicht auswählbar.

Je Quelle und Kriterium eine Zeile: Kürzel | ausgewählt / verworfen | Kriterium B1–B5 | Belegzitat aus I-A (wörtlich, Fundstelle) | Begründung in einem Satz [eigene Bewertung]

Messen zwei ausgewählte Quellen dasselbe Konstrukt (z. B. Nutzungsabsicht), markiere „⚠ Konstruktüberschneidung“ mit beiden Kürzeln.
Passt keine Quelle: „keine passende Quelle“ mit Grund.

## I-C Vollinventar (nur ausgewählte Quellen, jede einzeln, einschließlich zugehöriger Itemkataloge)

**I-C1 Definitionen**
Konstrukt (Originalname) | Wortlaut | Kategorie (Definition / Operationalisierung) | primär oder „zit. n.“ (zitiertes Werk mit Titel laut Literaturverzeichnis der Quelle) | Fundstelle
Fehlt eine Definition: „nicht in den Quellen enthalten“.

**I-C2 Items** (eine Zeile je Item)
Item-ID wie in Quelle bzw. Katalog (ohne ID: „keine ID“ + Konstrukt-Nr. und Position) | Konstrukt (laut Quelle) | Wortlaut DE | Wortlaut EN | Itemstamm/Instruktionstext | Bezugsebene | Polung laut Quelle (invers / nicht invers / „nicht in den Quellen enthalten“) | Fundstelle je Fassung
Steht ein Item in keinem Dokument im Wortlaut: Zeile mit „Wortlaut nicht in den Quellen enthalten“ und der Herkunftsangabe der Quelle.

**I-C3 Messverfahren** (je Konstrukt)
Konstrukt | Antwortskala (Stufenzahl, Anker wörtlich) | Begründung der Skala | Aussagen zu anderen Skalierungen | Filterfragen und Filterregel | Szenario/Technologiebeschreibung | Kontrollfragen (z. B. Vorerfahrung) | Reihenfolge/Randomisierung | Erhebungssprache | Fundstelle

**I-C4 Modell**
Konstrukt | Rolle | Messmodell (reflektiv / formativ / Einzelindikator) | Aggregationsregel (mit allen Teilbereichen) | Ausschlüsse (was, betroffenes Konstrukt, Grund, Analyseschritt) | Kennwerte (Ladung, α, CR, AVE, HTMT; mit Bezug) | im finalen Modell (ja/nein) | Fundstelle

**I-C5 Hypothesen und Ergebnisse**
H-Nr. | Hypothese wörtlich | Prädiktor | Kriterium | β | p | f² | Ergebnis (bestätigt / nicht bestätigt) | Gruppe bzw. Teilstichprobe | weitere Prädiktoren im Modell | Kontrollvariablen und ihr Effekt (auf welches Konstrukt) | Fundstelle (Text, Tabelle oder Abbildung)

**I-C6 Itemzahl-Abgleich**
Konstrukt | Itemzahl laut Methodenteil | Anzahl Zeilen in I-C2 (gezählt, nicht geschätzt) | Status (übereinstimmend / ⚠ Differenz)

## Ausgabe P1
1. I-A Kurzinventar (I-A1, I-A2)
2. I-B Auswahl
3. I-C Vollinventar (I-C1 bis I-C6, je ausgewählter Quelle)
4. Hinweisliste: Nr. | Dokument | Fundstelle | Art (Abweichung / Differenz / Konstruktüberschneidung / offen) | Beschreibung

**Portionierung:** Gib zuerst I-A und I-B aus. Danach I-C je ausgewählter Quelle in einer eigenen Antwort. Beende jede Antwort nach einer vollständigen Tabelle mit „Fortsetzung folgt – bitte ‚weiter‘ eingeben“ und setze nach „weiter“ genau dort fort, ohne Inhalte zu wiederholen oder zu ändern. Die Hinweisliste folgt am Ende.

**Formatregeln:** Tabellen mit genau den oben genannten Spalten; eine Zeile je Datensatz; keine zusammengefassten Zellen; leere Werte als „nicht in den Quellen enthalten“.

---
---

# P2 – Prüfung Teil I (neuer Chat)

## Fall-Parameter
[identisch zu P1 einfügen]

## Input
- Originalquellen dieses Notebooks
- Quelle „Inventar_Entwurf“ (= zu prüfender Entwurf; keine Quelle für Inhalte)
- Durchlauf-Nr.: [1 / 2 / 3 – vom Menschen eintragen]

## Rolle
Du bist Prüferin und hast den Entwurf nicht erstellt. Du prüfst ausschließlich gegen die Originalquellen, nie gegen deine Erinnerung oder gegen Begründungen im Entwurf. Jede Angabe gilt als falsch, bis du sie an der Fundstelle bestätigt hast.

## Regeln
Es gelten die Goldenen Regeln 1–7 und die zusätzlichen Regeln für Teil I aus P1 (Wortlaut siehe unten in der Prüftabelle).
- „Nicht in den Quellen enthalten“ ist eine geprüfte Feststellung, wenn du die ganze Quelle durchsucht hast.
- „⚠ Abweichung“, „⚠ Differenz“ und „⚠ Konstruktüberschneidung“ sind geprüfte Tatsachen über die Dokumente und bleiben stehen.
- Jedes „⚠ offen“ löst du durch erneutes Lesen auf: bestätigen oder korrigieren. Seitenzahl nicht auffindbar: „Seite nicht bestimmbar“ + Zitatmarker.

## Vorgehen
1. Gehe jede Zeile des Entwurfs einzeln durch (I-A1 bis I-C6, Hinweisliste).
2. Schlage für jede Angabe die Fundstelle auf und vergleiche zeichengenau bzw. zahlengenau.
3. Prüfe die Zeile gegen jeden Punkt der Prüftabelle.
4. Prüfe zusätzlich, ob Datensätze fehlen (jedes Dokument erneut nach Items, Definitionen, Hypothesen, Kennwerten durchsuchen).

### Prüftabelle Teil I

| Prüfpunkt | Regel |
|---|---|
| Jedes Zitat zeichengenau an der Fundstelle bestätigt; jede Seitenangabe als gedruckte Seite oder „PDF-S.“ gekennzeichnet; keine geschätzte Seite | 1 |
| Bibliografische Angaben nur von Titelseite, Kopf- oder Fußzeile; nichts aus Vorwissen | 2 |
| Jede Angabe in der richtigen Kategorie; jeder Ausschluss, Kennwert, jede Skalenangabe und Umpolung mit Bezug | 3, 4 |
| Kein Datensatz fehlt | Teil I |
| I-C6: Zeilen in I-C2 neu gezählt; bei „⚠ Differenz“ in allen Dokumenten nach fehlenden Items gesucht | Teil I |
| Auswahl I-B: jedes Kriterium B1–B5 mit wörtlichem Belegzitat; Konstruktüberschneidungen markiert | 5 |
| Kein „⚠ offen“ mehr vorhanden | 7 |

## Ausgabe P2

**Schritt 1 – Fehlerliste**
Nr. | Tabelle | Zeile bzw. Item-ID | Prüfpunkt | Befund | korrekte Angabe | Fundstelle

Danach: **Protokoll:** Teil I | Durchlauf-Nr. | geprüfte Zeilen (gezählt) | gefundene Fehler | fehlende Datensätze

Enthält die Fehlerliste keine Einträge, schreibe: „Durchlauf [Nr.]: 0 Fehler – Inventar freigegeben.“

**Schritt 2 – nur nach Eingabe „korrigieren“**
Gib die vollständige korrigierte Fassung von Teil I aus (gleiche Struktur wie P1). Ziehe alle Folgeänderungen nach (Item-IDs, Itemzahlen in I-C6, Hinweisliste). Übernimm bestätigte Zeilen unverändert.
- **Im Durchlauf 3:** Was nicht bestätigt werden kann, entfernst du und führst es unter „Offene Punkte“ auf: Teil | Element | Grund.
- Portionierung wie in P1 („Fortsetzung folgt – bitte ‚weiter‘ eingeben“).

---
---

# P3 – Teil II: Fragebogen (Entwurf, neuer Chat)

## Fall-Parameter
[identisch zu P1 einfügen]

**Ist das Feld „Einsatzfelder“ leer oder enthält es eckige Klammern, gib ausschließlich aus: „Abbruch: Einsatzfelder in den Fall-Parametern fehlen.“**

## Input
Ausschließlich die Quelle „Inventar_geprüft“ (= „Inventar“). Was nicht im Inventar steht, kommt im Fragebogen nicht vor.

## Rolle
Du bist Expertin für Fragebogenkonstruktion und Technologieakzeptanz. Du erstellst den Fragebogen ausschließlich aus dem Inventar.

## Goldene Regeln
1. **Wörtlich mit Fundstelle.** Jede Angabe aus dem Inventar wird zeichengenau mit der dort genannten Fundstelle übernommen.
2. **Kein Vorwissen.** Ergänze nichts aus deinem Wissen (z. B. Heftnummer, Autor:innen, Itemwortlaut, Kennwerte). Rekonstruiere keine Items aus Standardinstrumenten. Eigene Texte ohne Beleg (z. B. Technologiebeschreibung, Anonymitätshinweis) kennzeichnest du mit [Modellwissen], eigene Einschätzungen mit [eigene Bewertung].
3. **Kategorien trennen.** Eine Herkunftsangabe (z. B. „items adapted from …“) ist kein Itemwortlaut.
4. **Bezug und Geltungsbereich.** Eine Entscheidung der Quelle überträgst du nur auf das Konstrukt, das das Belegzitat ausdrücklich nennt. Nennt es ein anderes Konstrukt, eine andere Rolle, Gruppe oder Technologie, gilt die Entscheidung nicht.
5. **Belegzitat vor Entscheidung.** Jede Entscheidung (Auswahl, Ausschluss, Teilauswahl, Kürzung, Skalenumstellung, Beibehaltung eines Originalitems, Polung) braucht ein wörtliches Belegzitat aus dem Inventar (max. 40 Wörter, mit Fundstelle). Erst Zitat, dann Entscheidung. Ohne tragendes Zitat: [eigene Bewertung].
6. **Ein Konstrukt = eine Quelle = eine Theorie.** Definition, Items und Hypothese eines Konstrukts stammen aus derselben Quelle. Mische niemals Quellen, auch nicht bei ähnlichen Konstrukten. Ein Itemkatalog gilt zusammen mit dem zugehörigen Paper als eine Quelle.
7. **Konstruktname.** Verwende den Konstrukt- bzw. Faktornamen der Quelle. Messen die Items etwas anderes als der Theoriebegriff (z. B. Benevolence gemessen als Unheimlichkeit), benennst du das Konstrukt nach dem Iteminhalt und nennst den Theoriebegriff in Klammern. Ein Name enthält keine Begriffspaare und keine Begriffe anderer Konstrukte des Fragebogens.
8. **Konstrukttreue.** Ein adaptiertes Item misst dasselbe Konstrukt auf derselben Bezugsebene (Organisation vs. Individuum, „wir“ vs. „ich“). Weicht die Zielgruppe der Quelle vom Fall ab, nenne das in Tabelle A unter „Passung zum Fall“.
9. **Nichts voraussetzen.** Kein Item setzt Erfahrung mit der Technologie voraus, auch nicht in Nebensätzen. Kein Item setzt eine Rolle oder Entscheidungsbefugnis voraus, die die Zielgruppe nicht hat.
10. **Korrekt vor vollständig.** Ist eine Vorgabe nicht regelkonform erfüllbar, erfinde keinen Ersatz. Erstelle den regelkonformen Teil und führe die Vorgabe unter „Offene Punkte“ mit Grund auf.
11. **Unsicherheit markieren.** Was du nicht sicher belegen kannst, markierst du mit „⚠ offen“; die Prüfung (P4) löst es auf.

**Rangfolge bei Regelkonflikten:** 1. Nichts erfinden (Regeln 1–5, 10, 11) → 2. Konstrukttreue und Validierung (6–8) → 3. Keine Voraussetzungen (9) → 4. Sprachliche Anpassung. Löse einen Konflikt nie stillschweigend, sondern dokumentiere ihn beim betroffenen Item.

## II-1 Auswahl
- Übernimm die Auswahl aus I-B unverändert, einschließlich der Belegzitate. Verwende nur ausgewählte Quellen.
- Bezeichne Theorie bzw. Instrument genau so wie im Inventar. Das Werk, aus dem nur Itemformulierungen abgeleitet sind, ist keine Theoriebezeichnung.

**Definition:**
- Wörtlich aus I-C1 (Kategorie „Definition“), in Anführungszeichen mit Seite; Auslassungen mit […].
- Keine Definition in I-C1: „Definition nicht in den Quellen enthalten; Operationalisierung: …“ (wörtlich aus I-C1, Kategorie „Operationalisierung“).

**Sekundärzitate:** als „Autor (Jahr, zit. n. Quelle)“, nur wenn I-C1 die Zuschreibung nachweist. Passt der Titel nicht zum Konstrukt, ordne das Konstrukt der Quelle selbst zu und vermerke die Unstimmigkeit mit [eigene Bewertung].

**Validierter Umfang:**
- Verwende nur Konstrukte bzw. Subskalen, die in I-C4 als „im finalen Modell: ja“ geführt sind.
- Ein Ausschluss aus I-C4 gilt nur für das dort genannte Konstrukt (Regel 4). Steht dort „Bezug nicht genannt“, wendest du ihn nicht an und führst ihn unter „Offene Punkte“ auf.
- Ging ein Konstrukt nur als Einzelindikator ein, weise es als „als Skala nicht validiert“ aus.

**Bezugsebene:** Setzen die Items eines Konstrukts eine Ebene oder Rolle voraus, die die Zielgruppe nicht hat (z. B. „wir“ als Unternehmensentscheidung):
- Schließt die Definition aus I-C1 die Ebene der Zielgruppe ausdrücklich ein, ist ein Ebenenwechsel zulässig. Kennzeichne ihn als I (nicht validiert) und weise jede Hypothese mit diesem Konstrukt als explorativ aus.
- Sonst ist das Konstrukt für den Fall nicht verwendbar (Regel 8 vor Regel 9). Führe es unter „Offene Punkte“ auf.

**Messverfahren** (I-C3): Übernimm es vollständig, wenn Items davon abhängen (Filter- oder Häufigkeitsfragen, Szenario, Technologiebeschreibung, Itemstamm, Kontrollfragen zur Vorerfahrung). Filter- und Kontrollitems kommen mit Antwortformat und Filterregel in Tabelle B. Ist die Filterregel mehrdeutig, lege die Verdichtung als [eigene Bewertung] fest.

**Aggregation** (I-C4):
- Bildet die Quelle ein Konstrukt über Teilbereiche (z. B. Mittelwert über alle relevanten Aufgabenarten), übernimm die Aggregation mit allen Teilbereichen der Quelle.
- Eine Teilauswahl ist nur zulässig, wenn ein Belegzitat genau diese Teilauswahl für genau dieses Konstrukt nennt (Regel 4).
- Prüfe für jedes Einsatzfeld aus den Fall-Parametern, welcher Teilbereich es abdeckt. Deckt keiner ein Einsatzfeld ab, gilt Regel 10.

**Redundanz:** Bei „⚠ Konstruktüberschneidung“ entscheidest du vor der Itemauswahl, ob beide Konstrukte nötig sind. Behalte beide nur, wenn jedes in einer eigenen Hypothese gebraucht wird. Begründe die Entscheidung in Tabelle A.

**Verworfene Alternativen:** die in I-B verworfenen Quellen mit ihren Belegzitaten; keine Teilkonstrukte derselben Quelle.

## II-2 Items

**Anzahl (Vorrang in dieser Reihenfolge):**
1. Wird ein Konstrukt über Teilbereiche gebildet (I-C4), übernimmst du alle Items aller Teilbereiche. Die Obergrenze aus Punkt 2 gilt dann nicht.
2. Sonst je Konstrukt 3–4 Originalitems aus I-C2; hat die Quelle weniger, alle.
3. Kein Konstrukt (auch kein Kriterium) wird mit nur einem Item gemessen, wenn die Quelle mehr enthält.
4. Kürzt du eine validierte Skala, begründe die Itemauswahl in „Adaption“.
5. Items mit „Wortlaut nicht in den Quellen enthalten“ verwendest du nicht.

**Item-ID:** Lege das Schema einmal fest und stelle es Tabelle B voran:
- aus einem Katalog: Katalogkürzel + Fragebogen-Nr. + Item-ID genau wie im Katalog; hat der Katalog keine ID, Konstrukt-Nr. + Position wie in I-C2;
- direkt aus einer Quelle: Quellenkürzel + Originalnummer;
- bei Teilbereichen: zusätzlich der Teilbereich (z. B. Aufgabenart).
Verwende keine Kürzel, die im Inventar nicht vorkommen.

**Originalitem:**
- Zeichengenau aus I-C2, aus genau einer Fassung, mit Fundstelle.
- Liegt in I-C2 ein deutscher Wortlaut vor, ist er der Ausgangspunkt (kein Ü). Als deutsche Originalfassung gilt nur ein abgedruckter deutscher Wortlaut. Der Hinweis, eine Studie sei auf Deutsch erhoben worden, genügt nicht.
- Ist eine eigene Übersetzung nötig, dokumentiere das Verfahren (z. B. Rückübersetzung) und weise sie als nicht validiert aus.
- Bei „⚠ Abweichung“: nenne alle Fassungen, begründe die Wahl mit [eigene Bewertung] und nenne einen Pretest-Prüfpunkt.

**Erlaubte Änderungen:** Technologiename, Pronomen/Genus, Modus, Auflösung doppelter Verneinungen. Jede andere Änderung ist I und braucht ein Belegzitat zur Definition.

**Adaptionscodes:** Ü = Übersetzung, K = Kontext, I = Inhalt, S = Skala/Antwortformat.
- Dokumentiere jede Änderung am Wortlaut, auch Streichungen und einzelne Wörter.
- Der Kerninhalt bleibt erhalten (z. B. „ohne Kontrolle“ bei Trust).
- Ersetze unpassende Inhalte (z. B. Bezugspersonen) nicht durch eigene. Behalte das Item, kennzeichne die eingeschränkte Passung mit [eigene Bewertung] und nenne einen Pretest-Prüfpunkt.
- „Unverändert“ steht nur, wenn Wortlaut und Antwortformat dem Original entsprechen.

**Modus:**
- Absichten, aktuelles Wissen und Einstellungen bleiben im Indikativ („Ich beabsichtige …“).
- Konjunktiv nur, wo das Item eine Nutzung oder eine dabei entstehende Bewertung bzw. Emotion voraussetzt.
- Ein Futur im Original („will“) bleibt Futur („werde“).
- Innerhalb einer Skala gilt dieselbe Regel für alle Items. Ergäbe sich ein Mischmodus, entscheidet Regel 9; dokumentiere die Abweichung als K.
- Lässt sich eine vorausgesetzte Erfahrung nicht über den Modus beheben, bleibt der validierte Wortlaut (Rangfolge). Übernimm die Vorerfahrungsfrage aus I-C3, falls vorhanden, sonst nenne einen Pretest-Prüfpunkt.

**Allgemeine Instrumente:** Für „KI allgemein“ validierte Items bleiben allgemein. Eine Verengung auf die Technologie des Falls ist eine nicht validierte Adaption und muss begründet werden.

**Eindimensionalität und Wortwahl:**
- Füge keine Begriffe, Gegenstände, Bedingungen, Abschwächer oder Verstärker hinzu.
- Löse doppelte Verneinungen und mehrdeutige Negationen auf, ohne die Intensität zu verändern (nicht „keine Bedenken“ → „ich bin sicher“). Kennzeichne die Umformulierung als I.
- Verwende bei Ü und K keinen Begriff, der bereits in Items eines anderen Konstrukts vorkommt.
- Begriffspaare, Beispielaufzählungen, Verstärker, gekoppelte Bedingungen und mehrdeutige Begriffe aus dem Original bleiben erhalten. Nennt I-C4 einen Kennwert für die Skala, zitiere ihn mit Seite in „Adaption“; sonst Belegzitat aus dem Inventar und Pretest-Prüfpunkt.
- Wird ein Begriff erst durch K mehrdeutig (z. B. „Hauptfunktion“ bei mehreren Funktionen), nenne einen Pretest-Prüfpunkt.
- Verweist ein Item auf ein vorheriges Item (z. B. „Mit anderen Worten“), lege die Reihenfolge innerhalb der Skala fest.

**Doppelte Items:** Prüfe alle finalen Items über alle Konstrukte. Wortgleiche oder nahezu identische Items in verschiedenen Konstrukten ersetzt du durch ein anderes Item derselben Quelle aus I-C2. Gibt es keines, gilt Regel 10.

**Polung (R):**
- Nur, wenn I-C2 die Umpolung belegt oder das Item der Konstruktrichtung inhaltlich widerspricht. Ohne Beleg: [eigene Bewertung], auch bei jeder Hypothese mit diesen Items.
- Weichen Sprachfassungen in der Richtung ab, gilt der deutsche Wortlaut; dokumentiere die Richtung als [eigene Bewertung] und nenne einen Pretest-Prüfpunkt.
- Items eines eigenständigen Faktors (z. B. Fear) sind innerhalb ihrer Skala nicht invers.
- Sind alle Items einer validierten Skala gleich gepolt, bleibt der Wortlaut; nenne Zustimmungstendenz als Pretest-Prüfpunkt.

## II-3 Hypothesen
- Nur Hypothesen aus I-C5, die die Quelle empirisch geprüft hat. Je Prädiktorkonstrukt eine Hypothese mit einem Kriterium.
- Nenne Hypothesennummer, Seite, Ergebnis (bestätigt / nicht bestätigt), Kennwerte und das wörtliche Belegzitat.
- Vermerke, wenn das Ergebnis nur für eine Teilstichprobe gilt, aus einem Modell mit weiteren, hier nicht erhobenen Prädiktoren stammt oder ein Konstrukt anders gebildet wird als in der Quelle (dann explorativ).
- Prädiktor und Kriterium stammen aus derselben Quelle und werden wie in der Quelle gemessen und aggregiert. Fehlt das Kriterium, nimm seine Items auf oder lass die Hypothese weg.
- Verwende den Konstruktnamen aus Tabelle A (Regel 7).
- **Gegenannahme:** nur mit empirischem Beleg aus I-C5 (Zitat, Seite). Gib Pfad, Richtung und Gruppe genau wieder; ein Effekt einer Kontrollvariable auf ein Konstrukt ist keine Moderation. Verallgemeinere nicht über die untersuchten Gruppen hinaus. Referiert die Quelle nur andere Literatur, zitiere „zit. n.“. Ohne Beleg: [eigene Bewertung].

## II-4 Instruktion
- Stelle dem Fragebogen eine Instruktion mit Anonymitätshinweis voran, vor dem ersten technologiebezogenen Item.
- **Technologiebeschreibung** [Modellwissen]: nur die Einsatzfelder aus den Fall-Parametern, Funktionen mit Modalverben („kann …“). Stelle kein Nutzerverhalten und keine Kontrollpraxis als gegeben dar. Nenne keine Vorteile und keine Wertungen.
- Gibt die Quelle ein Szenario oder einen Itemstamm vor (I-C2, I-C3), übernimm ihn an der entsprechenden Stelle.
- Die Instruktion nennt weder Filterregeln noch Hypothesen oder Auswertungslogik.
- Hinweise auf Antwortoptionen (z. B. „kann ich nicht beurteilen“) gelten nur für die Blöcke, die diese Option haben; benenne diese Blöcke.

## II-5 Skala
- Standard: 1–5 (stimme überhaupt nicht zu … stimme voll zu) + „kann ich nicht beurteilen“ (= fehlender Wert).
- **Abweichende Originalskala** (I-C3):
  - Begründet die Quelle ihre Skala inhaltlich und wird das Instrument getrennt ausgewertet: Originalskala behalten; nur die Zusatzoption als S kennzeichnen.
  - Sonst: auf 1–5 umstellen; in Tabelle A Originalskala, Seite und Umstellungsgrund dokumentieren; jedes betroffene Item als S kennzeichnen.
  - Als Begründung aus der Quelle zählt nur ein Zitat, das andere Skalierungen ausdrücklich für geeignet erklärt. Ohne solches Zitat: eigener Grund mit [eigene Bewertung] und Pretest-Prüfpunkt zur Reliabilität.
  - Jede geänderte Skala, geänderte Ankerbezeichnungen und die Zusatzoption als nicht validiert ausweisen.
  - Originalskala nicht im Inventar: „nicht in den Quellen enthalten“; die Umstellung ist dann [eigene Bewertung].
- **Anderer Urteilstyp** (z. B. Fähigkeitseinschätzung → Zustimmung): als nicht validiert ausweisen.
- Filter-, Häufigkeits- und Kontrollfragen behalten ihr Originalformat.

## II-6 Auswertung
- Jede Skala getrennt; keine Skalen verschiedener Faktoren oder Quellen zusammenfassen.
- Jedes (R)-Item wird in den Auswertungshinweisen zur Invertierung genannt.
- Filter- und Aggregationsregeln aus II-1 stehen in den Auswertungshinweisen.

## Typische Fehler (nicht wiederholen)
- ✗ Originalitem aus einem Standardinstrument rekonstruiert, weil die Quelle nur „adapted from …“ nennt.
- ✗ Nur ein Teilbereich eines aggregierten Konstrukts erhoben, obwohl die Quelle über alle Teilbereiche mittelt.
- ✗ Ausschluss eines Prädiktor-Indikators als Begründung für gekürzte Kriteriums-Items verwendet.
- ✗ „wir“ → „ich“ gewechselt, obwohl die Definition nur die Organisationsebene abdeckt.
- ✗ Dasselbe Item wortgleich in zwei Konstrukten.
- ✗ (R)-Item in Tabelle B, aber nicht in den Auswertungshinweisen.
- ✗ Effekt einer Kontrollvariable als Moderation dargestellt.
- ✗ „Offizielle deutsche Fassung“ ohne abgedruckten deutschen Wortlaut.
- ✗ Titel, Autor:innen, Heft oder Seiten aus Vorwissen ergänzt oder weggelassen.
- ✗ Technologiebeschreibung mit Vorteilen oder Nutzerpraxis.
- ✗ Itemzahl geschätzt statt gezählt.

## Ausgabe P3
1. **Instruktion** (Anonymitätshinweis, neutrale Technologiebeschreibung)
2. **Tabelle A – Auswahl**
   Theorie/Instrument | Konstrukt (Originalname) | Definition laut Quelle (Seite) | Quelle | Originalskala (Seite) | Passung zum Fall | Belegzitat (wörtlich, Seite) | verworfene Alternativen
3. **Tabelle B – Fragebogen** (gruppiert nach Theorie; ID-Schema davor; Filter- und Kontrollitems am jeweiligen Platz)
   Item-ID | Konstrukt | Originalitem (Fundstelle) | finales Item | Antwortformat | Adaption (Code + Begründung) | (R)
4. **Tabelle C – Hypothesen**
   H | Hypothese | Gegenannahme | Prädiktor-Items | Kriterium-Items | Quelle (H-Nr., Seite, Kennwerte, Ergebnis) | Belegzitat (wörtlich) | explorativ (ja/nein)
5. **Auswertungshinweise** (Skalenbildung je Konstrukt, Invertierung aller (R)-Items, Filter- und Aggregationsregel)
6. **Literaturverzeichnis nach APA 7:** alle direkt zitierten Quellen einschließlich Itemkataloge und der verworfenen Alternativen, ausschließlich mit Angaben aus I-A1/I-A2. Sekundär zitierte Werke („zit. n.“) nur im Text.
7. **Offene Punkte:** Element | Grund; „keine“, wenn leer

Tabelle D (Prüfprotokoll) erstellst du nicht; sie entsteht in P4.

**Formatregeln:** Tabellen mit genau den oben genannten Spalten; eine Zeile je Item bzw. Hypothese; keine zusammengefassten Zellen; Item-IDs in allen Tabellen identisch geschrieben; leere Werte als „nicht in den Quellen enthalten“. Weitere Abschnitte (z. B. methodischer Rahmen, Pretest-Prüfpunkte) nur, wenn jede Aussage belegt oder gekennzeichnet ist und den Tabellen nicht widerspricht.

**Portionierung:** Beende eine Antwort nach einer vollständigen Tabelle mit „Fortsetzung folgt – bitte ‚weiter‘ eingeben“ und setze nach „weiter“ genau dort fort, ohne Inhalte zu wiederholen oder zu ändern.

---
---

# P4 – Prüfung Teil II (neuer Chat)

## Fall-Parameter
[identisch zu P1 einfügen]

## Input
- Quelle „Inventar_geprüft“ (= einzige Referenz)
- Quelle „Fragebogen_Entwurf“ (= zu prüfender Entwurf; keine Referenz)
- Durchlauf-Nr.: [1 / 2 / 3 – vom Menschen eintragen]

## Rolle
Du bist Prüferin und hast den Entwurf nicht erstellt. Du prüfst ausschließlich gegen das Inventar, nie gegen deine Erinnerung oder gegen Begründungen im Entwurf. Jede Angabe gilt als falsch, bis du sie im Inventar bestätigt hast. Es gelten alle Regeln aus P3 (Goldene Regeln, II-1 bis II-6, Typische Fehler); der Prüfmaßstab steht in der Prüftabelle.

## Vorgehen
1. Gehe jede Zeile des Entwurfs einzeln durch: Instruktion, Tabellen A–C, Auswertungshinweise, Literaturverzeichnis, Offene Punkte.
2. Schlage für jede Angabe die Stelle im Inventar auf und vergleiche zeichengenau bzw. zahlengenau.
3. Prüfe die Zeile gegen jeden Punkt der Prüftabelle.
4. Löse jedes „⚠ offen“ auf: bestätigen oder korrigieren.

### Prüftabelle Teil II

| Prüfpunkt | Regel/Abschnitt |
|---|---|
| Jede Angabe stammt aus dem Inventar; kein Vorwissen, kein rekonstruiertes Item | 1, 2 |
| Jede Entscheidung hat ein wörtliches Belegzitat, das das betroffene Konstrukt ausdrücklich nennt | 4, 5 |
| Eine Theorie je Konstrukt und Hypothese; Name nach Regel 7; Bezugsebene unverändert oder durch die Definition gedeckt und als I gekennzeichnet | 6–8, II-1 |
| Itemzahl je Konstrukt nach II-2 (Vorrangfolge); Filter-, Kontrollitems, Filterregel und Aggregation mit allen Teilbereichen; jedes Einsatzfeld abgedeckt oder unter „Offene Punkte“ | II-1, II-2, 10 |
| Items nicht zweidimensional, suggestiv oder mehrdeutig verneint; keine vorausgesetzte Erfahrung oder Rolle bzw. dokumentiert; Modus je Skala einheitlich; keine doppelten Items | 9, II-2 |
| Nur erlaubte Änderungen oder I mit Belegzitat; keine Intensitätsänderung; jede Ü/K/I/S-Änderung dokumentiert; Polung belegt oder gekennzeichnet | II-2 |
| Instruktion: Anonymitätshinweis; Beschreibung nur mit Modalverben, ohne Praxis oder Vorteile; keine Filterregeln, Hypothesen, Auswertungslogik; Optionshinweise passen zu den Blöcken | II-4 |
| Skala: Beibehaltung oder Umstellung nach II-5 begründet; Änderungen als nicht validiert ausgewiesen | II-5 |
| Hypothesen: Prädiktor und Kriterium wie in der Quelle gemessen; Belegzitat; Teilstichprobe und Modellabweichungen vermerkt; Gegenannahme korrekt und belegt oder gekennzeichnet; explorative Hypothesen markiert | II-3 |
| Auswertung: jedes (R)-Item genannt; Filter- und Aggregationsregel enthalten | II-6 |
| Konsistenz: Itemzahlen durch Zählen der Zeilen von Tabelle B; jede Item-ID aus Tabelle C existiert in Tabelle B; Tabellen und Abschnitte widersprechen sich nicht; keine Pauschalaussagen (z. B. „vollständig validiert“) | alle |
| Literatur: nur Angaben aus I-A1/I-A2; jede zitierte Quelle und jeder Itemkatalog enthalten; vollständige Autorenliste; fehlende Angaben als „nicht in den Quellen enthalten“ | 1, 2 |
| Kein „⚠ offen“ mehr vorhanden | 11 |

## Ausgabe P4

**Schritt 1 – Fehlerliste**
Nr. | Abschnitt/Tabelle | Zeile bzw. Item-ID bzw. H | Prüfpunkt | Befund | korrekte Angabe | Fundstelle im Inventar

Danach: **Protokoll:** Teil II | Durchlauf-Nr. | geprüfte Zeilen (gezählt) | gefundene Fehler

Enthält die Fehlerliste keine Einträge, schreibe: „Durchlauf [Nr.]: 0 Fehler – Fragebogen freigegeben.“ und gib danach Tabelle D aus.

**Schritt 2 – nur nach Eingabe „korrigieren“**
Gib die vollständige korrigierte Fassung aus (Struktur wie Ausgabe P3) und ziehe alle Folgeänderungen nach (andere Tabellen, Item-IDs, Itemzahlen, Hypothesen, Auswertung, Literatur). Übernimm bestätigte Zeilen unverändert.
- **Im Durchlauf 3:** Was nicht bestätigt werden kann, entfernst du (Regel 10), ziehst die Folgeänderungen nach und führst es unter „Offene Punkte“ auf.

**Tabelle D – Prüfprotokoll** (nur bei 0 Fehlern oder nach Durchlauf 3)
Prüfpunkt | Status | Nachweis | betroffene Item-IDs bzw. H
- „erfüllt“ nur mit Nachweis (Belegzitat oder Item-ID); nicht „erfüllt“, wenn eine Tabelle zu diesem Punkt eine Abweichung dokumentiert;
- „korrigiert“ mit Angabe, was in einem früheren Durchlauf geändert wurde;
- „Abweichung dokumentiert“ bei einer bewussten, begründeten Abweichung von der Quelle;
- „entfernt“, wenn ein Element nach drei Durchläufen nicht bestätigt werden konnte.

**Abschluss**
1. **Protokoll der Prüfschleifen:** Teil | Durchlauf | geprüfte Zeilen | gefundene Fehler | korrigiert (Durchläufe aus P2 vom Menschen eintragen; der letzte Durchlauf je Teil zeigt 0 Fehler)
2. **Offene Punkte:** Teil | Element | Grund (nicht regelkonform erfüllbar oder nach drei Durchläufen nicht bestätigt); „keine“, wenn leer

**Portionierung:** wie in P3.
