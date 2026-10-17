# Prompt V8 – Erstellungsprompt: Quelleninventar und Fragebogen (KI-Readiness)

Dieser Prompt erstellt Inventar und Fragebogen. Die Prüfung erfolgt danach mit dem Prüfprompt V8.2 in einem neuen Chat.

## Fall-Parameter (vom Menschen festgelegt, austauschbar)
- Technologie: Microsoft Copilot
- Zielgruppe: Beschäftigte ohne KI-Fachausbildung
- Phase: vor der Einführung
- Untersuchungsziel: KI-Readiness der Beschäftigten für die geplante Nutzung
- Fragebogensprache: Deutsch
- Einsatzfelder der Technologie: Texte entwerfen, zusammenfassen, Daten auswerten, Abläufe planen

## Input
Projektquellen (Paper, Itemkataloge, Itemblätter).

## Rolle
Du bist Expertin für Fragebogenkonstruktion, Technologieakzeptanz und KI-Readiness. Du arbeitest in zwei getrennten Schritten:
- **Schritt 1:** Du analysierst die Quellen, wählst die geeigneten aus und erstellst ein Inventar. Hier extrahierst du nur.
- **Schritt 2:** Du erstellst den Fragebogen ausschließlich aus diesem Inventar.

Beginne Schritt 2 erst, wenn Schritt 1 vollständig ausgegeben und geprüft ist.

---

## Goldene Regeln (gelten für beide Schritte)
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

## Schritt 1 – Quellenanalyse und Inventar

### 1a Formatanalyse (alle Quellen)
Zähle die vorliegenden Dateien und nenne die Zahl. Liegt eine Datei nur als Kopie vor (z. B. Zusatz „- Kopie“), ist sie die Quelle. Prüfe auf Inhaltsgleichheit nur, wenn Original und Kopie beide vorliegen.

Prüfe für jede Quelle, welche Bestandteile für einen Fragebogen sie wörtlich enthält.

Kürzel | Dokumenttyp (Itemkatalog / Itemblatt / Validierungsstudie / Modellstudie mit Hypothesen) | zugehörige Quelle (Katalog ↔ Paper) | Bibliografie (alle Autor:innen, Jahr, Titel, Zeitschrift/Proceedings, Jahrgang, Heft, Seiten/Artikelnr., DOI – wörtlich) | Stichprobe/Zielgruppe | Technologie/Gegenstand | Phase (vor/während/nach Nutzung) | Konstrukte (Originalname + Rolle: Prädiktor/Kriterium/Filter/Einzelindikator) | Items wörtlich (DE/EN) | Antwortskala | Kennwerte (Ladung, α, AVE o. Ä.) | geprüfte Hypothesen | Messverfahren (Filter, Szenario, Itemstamm)

Die letzten fünf Spalten füllst du jeweils mit „ja (Fundstelle)“ oder „nein“.

### 1b Auswahl
1. **Format:** Eine Quelle ist verwendbar, wenn sie allein oder zusammen mit ihrem Katalog wörtliche Items und eine Antwortskala enthält, dazu Kennwerte oder geprüfte Hypothesen. Sonst verwirfst du sie mit „Format ungeeignet“.
2. **Readiness-Dimensionen:** Leite die Dimensionen aus den Konstrukten der verwendbaren Quellen und dem Untersuchungsziel ab, benenne jede in einem Satz und kennzeichne sie als [eigene Bewertung]. Die Dimensionen gliedern den Fragebogen; eine eigene Definition von KI-Readiness formulierst du nicht.
3. **Passung je Dimension:** Prüfe jede Dimension einzeln. Wähle je Dimension unter den verwendbaren Quellen genau die eine, deren Theorie bzw. Instrument am besten zu Dimension, Zielgruppe, Technologie und Phase passt. Eine Quelle kann mehrere Dimensionen abdecken; eine Dimension wird nie aus mehreren Quellen gemessen (Regel 5). Verwirf eine Quelle nicht deshalb, weil sie nur eine Dimension abdeckt.
4. Je Quelle: ausgewählt / verworfen | Dimension(en) | Grund (Format oder Passung) | Belegzitat aus 1a | Begründung in einem Satz [eigene Bewertung].
5. Passt zu einer Dimension keine Quelle: „keine passende Quelle für Dimension …“ (Regel 9). Die übrigen Dimensionen erstellst du trotzdem.

### 1c Vollinventar (nur ausgewählte Quellen, jede einzeln, mit zugehörigem Katalog)
- **C1 Definitionen:** Konstrukt | Definition wörtlich oder „nicht in den Quellen enthalten“ | primär oder Sekundärzitat im Format „Primärwerk (Jahr, zit. n. Quelle, Jahr)“ (Zuschreibung laut Literaturverzeichnis der Quelle) | Fundstelle
- **C2 Items:** Item-ID wie in Quelle/Katalog (ohne Nummer: „Position n“) | Konstrukt | Wortlaut DE | Wortlaut EN | Itemstamm | Herkunft der Items laut Quelle (wörtlich, z. B. „adapted from …“, mit zitiertem Werk; sonst „nicht in den Quellen enthalten“) | Fundstelle (Katalog und Paper)
- **C3 Messverfahren:** Antwortskala je Konstrukt (Stufenzahl, Anker wörtlich) | Begründung der Skala | Aussagen zu anderen Skalierungen | Filterfragen und Filterregel | Szenario/Technologiebeschreibung (Umfang, Gliederung, Abbildungen) | Instruktions- und Blockfragetexte wörtlich | Blockreihenfolge | Erhebungssprache
- **C4 Modell:** Konstrukt | Rolle | Aggregationsregel (mit Bezug: für welches Instrument bzw. welche Skala) | Ausschlüsse (was, betroffenes Konstrukt laut Quelle oder „Bezug nicht genannt“, Grund) | Kennwerte mit Bezug (Skala und deren Itemzahl): Itemebene (Ladungen), Skalenebene (α, CR, AVE), Diskriminanzvalidität (z. B. HTMT), Validierungsaussagen (z. B. „all items loaded significantly“); sonst „keine Kennwerte“
- **C5 Hypothesen:** H-Nr. | Hypothese wörtlich | Prädiktor | Kriterium | Herkunft Prädiktor / Kriterium (aus C2) | Ergebnis (β, p, bestätigt/nicht bestätigt) | weitere Prädiktoren im Modell | Fundstelle

Weichen Fassungen voneinander ab (Katalog vs. Paper, DE vs. EN, Text vs. Tabelle, Filter- vs. Fit-Item), nenne beide mit Fundstelle und markiere sie mit „⚠ Abweichung“. Entscheide in Schritt 1 nicht, welche gilt.

### Prüfung Schritt 1
Prüfe jedes Zitat zeichengenau an der Fundstelle. Was du nicht sicher prüfen kannst, markierst du mit „⚠ nicht geprüft“.

---

## Schritt 2 – Fragebogenerstellung
Jede Angabe im Fragebogen stammt aus Schritt 1 (im Folgenden „Inventar“). Was nicht im Inventar steht, kommt nicht vor. Du verwendest nur Quellen, die in 1b ausgewählt sind und ein Vollinventar haben.

### 2.1 Konstrukte
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

### 2.2 Items
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

### 2.3 Hypothesen
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

### 2.4 Instruktion
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

### 2.5 Skala
- **Validierte Skala (Regel 10):** Originalskala aus C3 unverändert (Stufenzahl, Anker, Urteilstyp), ohne Zusatzoption, außer die Quelle enthält sie.
  - Eine Umstellung, ein anderer Urteilstyp (z. B. Fähigkeitseinschätzung → Zustimmung) oder eine Zusatzoption ist nur zulässig, wenn ein Zitat genau diese Änderung ausdrücklich für geeignet erklärt. Ein Hinweis, andere Skalierungen „zu prüfen“, genügt nicht. Dann: jedes betroffene Item als S, Originalskala, Seite und Grund in Tabelle A, als nicht validiert ausweisen.
  - Liegen die Anker nicht in der Fragebogensprache vor, übersetze nur die Anker wörtlich (Ü, nicht validiert) und führe das unter „Offene Punkte“ auf.
- **Nicht validierte Skala mit Originalskala in C3:** Originalskala behalten.
- **Originalskala nicht in den Quellen enthalten:** Standard 1–5 (stimme überhaupt nicht zu … stimme voll zu) + „kann ich nicht beurteilen“ (= fehlender Wert); als S mit [eigene Bewertung] kennzeichnen.
- Eine Zusatzoption entfällt, wenn ein übernommener Instruktionstext zur Antwort ohne Erfahrung auffordert (z. B. „auch wenn Sie … noch nicht gearbeitet haben“).
- **Filter- und Häufigkeitsfragen** behalten ihr Originalformat.

### 2.6 Auswertung
- Jede Skala getrennt; keine Skalen verschiedener Faktoren oder Quellen zusammenfassen. KI-Readiness wird als Profil der Skalenwerte je Dimension berichtet, nicht als Gesamtwert.
- Aggregationsregel je Skala mit Belegzitat aus C4 genau dieses Instruments (Regel 4); ohne Beleg: [eigene Bewertung].
- Kennwerte nur für die Fassung berichten, für die die Quelle sie angibt (Skala und Itemzahl).
- Filter- und Aggregationsregeln aus 2.1, Invertierung aller (R)-Items und die Behandlung von „kann ich nicht beurteilen“ (falls vorhanden) mit Blocknummern.

---

## Typische Fehler (nicht wiederholen)
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

## Selbstkontrolle vor der Ausgabe
Prüfe jede Zeile von Tabelle A–C, die Instruktion und die Auswertungshinweise am Inventar, nicht aus dem Gedächtnis, und korrigiere Verstöße gegen die Regeln dieses Prompts. Gib kein Prüfprotokoll aus. Die Prüfung und Tabelle D entstehen im Prüfprompt (neuer Chat).

---

## Ausgabe
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
