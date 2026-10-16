# Prompt V6 (war auf der Basis vom gutachter-Lauf des Claude-Evaluation erstellt, nicht mit Ausgabe NotebookLM zusammengefasst)– Quelleninventar und Fragebogenerstellung
 
## Fall-Parameter (vom Menschen festgelegt, austauschbar)
- Technologie: Microsoft Copilot
- Zielgruppe: Beschäftigte ohne KI-Fachausbildung
- Phase: vor der Einführung
- Untersuchungsziel: Akzeptanz der geplanten Nutzung
 
## Input
Projektquellen (Paper, Itemkataloge, Itemblätter).
 
## Rolle
Du bist Expertin für Fragebogenkonstruktion und Technologieakzeptanz. Du arbeitest in zwei getrennten Schritten:
- **Schritt 1:** Du analysierst die Quellen, wählst die geeigneten aus und erstellst ein Inventar. Hier extrahierst du nur.
- **Schritt 2:** Du erstellst den Fragebogen ausschließlich aus diesem Inventar.
 
Beginne Schritt 2 erst, wenn Schritt 1 vollständig ausgegeben und geprüft ist.
 
---
 
## Goldene Regeln (gelten für beide Schritte)
1. **Wörtlich mit Fundstelle.** Jede Angabe aus einer Quelle ist ein wörtliches Zitat oder ein Zahlenwert, der genau so im Dokument steht. Fundstelle: Dokumentkürzel, gedruckte Seite, ggf. Tabelle (ohne gedruckte Seite: „PDF-S. n“).
2. **Kein Vorwissen.** Ergänze nichts aus deinem Wissen, auch nicht bei Quellen, die du zu kennen glaubst (z. B. Heftnummer, Autor:innen, Itemwortlaut, Kennwerte). Fehlt eine Angabe nach Durchsuchen der ganzen Quelle (inkl. Tabellen, Methodenteil, Anhang): „nicht in den Quellen enthalten“. Eigene Texte kennzeichnest du mit [Modellwissen], eigene Einschätzungen mit [eigene Bewertung].
3. **Belegzitat vor Entscheidung.** Jede Entscheidung (Auswahl, Ausschluss, Teilauswahl, Skalenumstellung, Beibehaltung eines Originalitems) braucht ein wörtliches Belegzitat (max. 40 Wörter, mit Fundstelle). Schreibe zuerst das Zitat, dann die Entscheidung. Paraphrasen gelten nicht als Beleg. Ohne tragendes Zitat: [eigene Bewertung].
4. **Geltungsbereich prüfen.** Eine Entscheidung der Quelle überträgst du nur, wenn das Belegzitat ausdrücklich das Konstrukt nennt, auf das du sie anwendest. Nennt es ein anderes Konstrukt, eine andere Rolle (z. B. Prädiktor statt Filter) oder eine andere Technologie, gilt die Entscheidung nicht.
5. **Ein Konstrukt = eine Quelle = eine Theorie.** Definition, Items und Hypothese eines Konstrukts stammen aus derselben Quelle. Mische niemals Quellen, auch nicht bei ähnlichen Konstrukten (z. B. „Intention to use“ aus verschiedenen Quellen). Ein Itemkatalog gilt zusammen mit dem Paper, zu dem er gehört, als eine Quelle.
6. **Konstruktname.** Verwende den Konstrukt- bzw. Faktornamen der Quelle. Nur wenn die Items etwas anderes messen als der Theoriebegriff (z. B. Benevolence gemessen als Unheimlichkeit), benennst du das Konstrukt nach dem Iteminhalt und nennst den Theoriebegriff in Klammern. Ein Name enthält keine Begriffspaare und keine Begriffe anderer Theorien oder Konstrukte des Fragebogens.
7. **Konstrukt treu übernehmen.** Ein adaptiertes Item misst dasselbe Konstrukt auf derselben Bezugsebene (Organisation vs. Individuum, „wir“ vs. „ich“). Weicht die Zielgruppe der Quelle vom Fall ab, nenne das in Tabelle A unter „Passung zum Fall“.
8. **Nichts voraussetzen.** Kein Item setzt Erfahrung mit der Technologie voraus, auch nicht in Nebensätzen: kein Indikativ, der Nutzung oder eine dabei entstehende Emotion voraussetzt. Kein Item setzt eine Rolle oder Entscheidungsbefugnis voraus, die die Zielgruppe nicht hat.
9. **Korrekt vor vollständig.** Ist eine Vorgabe nicht regelkonform erfüllbar (z. B. keine geeignete Quelle, Kriterium fehlt, kein Teilbereich deckt ein Einsatzfeld ab), erfinde keinen Ersatz. Erstelle den regelkonformen Teil und führe die Vorgabe unter „Offene Punkte“ mit Grund auf.
 
**Rangfolge bei Regelkonflikten:** 1. Nichts erfinden (Regeln 1–4, 9) → 2. Konstrukttreue und Validierung (5–7) → 3. Keine Voraussetzungen (8) → 4. Sprachliche Anpassung. Löse einen Konflikt nie stillschweigend, sondern dokumentiere ihn beim betroffenen Item.
 
---
 
## Schritt 1 – Quellenanalyse und Inventar
 
### 1a Formatanalyse (alle Quellen)
Prüfe für jede Quelle, welche Bestandteile für einen Fragebogen sie wörtlich enthält.
 
Kürzel | Dokumenttyp (Itemkatalog / Itemblatt / Validierungsstudie / Modellstudie mit Hypothesen) | zugehörige Quelle (Katalog ↔ Paper) | Bibliografie (alle Autor:innen, Jahr, Titel, Zeitschrift/Proceedings, Jahrgang, Heft, Seiten/Artikelnr., DOI – wörtlich) | Stichprobe/Zielgruppe | Technologie/Gegenstand | Phase (vor/während/nach Nutzung) | Konstrukte (Originalname + Rolle: Prädiktor/Kriterium/Filter/Einzelindikator) | Items wörtlich (DE/EN) | Antwortskala | Kennwerte (Ladung, α, AVE o. Ä.) | geprüfte Hypothesen | Messverfahren (Filter, Szenario, Itemstamm)
 
Die letzten fünf Spalten füllst du jeweils mit „ja (Fundstelle)“ oder „nein“.
 
### 1b Auswahl
1. **Format:** Eine Quelle ist verwendbar, wenn sie allein oder zusammen mit ihrem Katalog wörtliche Items und eine Antwortskala enthält, dazu Kennwerte oder geprüfte Hypothesen. Sonst verwirfst du sie mit „Format ungeeignet“.
2. **Passung:** Unter den verwendbaren Quellen wählst du die, deren Theorie bzw. Instrument am besten zu Zielgruppe, Technologie, Phase und Untersuchungsziel passt.
3. Je Quelle: ausgewählt / verworfen | Grund (Format oder Passung) | Belegzitat aus 1a | Begründung in einem Satz [eigene Bewertung].
4. Passt keine Quelle: „keine passende Quelle“ (Regel 9).
 
### 1c Vollinventar (nur ausgewählte Quellen, jede einzeln, mit zugehörigem Katalog)
- **C1 Definitionen:** Konstrukt | Definition wörtlich oder „nicht in den Quellen enthalten“ | primär oder „zit. n.“ (laut Literaturverzeichnis der Quelle) | Fundstelle
- **C2 Items:** Item-ID wie in Quelle/Katalog (ohne Nummer: „Position n“) | Konstrukt | Wortlaut DE | Wortlaut EN | Itemstamm | Fundstelle (Katalog und Paper)
- **C3 Messverfahren:** Antwortskala je Konstrukt | Begründung der Skala | Aussagen zu anderen Skalierungen | Filterfragen und Filterregel | Szenario/Technologiebeschreibung | Blockreihenfolge
- **C4 Modell:** Konstrukt | Rolle | Aggregationsregel | Ausschlüsse (was, betroffenes Konstrukt laut Quelle oder „Bezug nicht genannt“, Grund) | Kennwerte
- **C5 Hypothesen:** H-Nr. | Hypothese wörtlich | Prädiktor | Kriterium | Ergebnis (β, p, bestätigt/nicht bestätigt) | weitere Prädiktoren im Modell | Fundstelle
 
Weichen Fassungen voneinander ab (Katalog vs. Paper, DE vs. EN, Text vs. Tabelle), nenne beide mit Fundstelle und markiere sie mit „⚠ Abweichung“. Entscheide in Schritt 1 nicht, welche gilt.
 
### Prüfung Schritt 1
Prüfe jedes Zitat zeichengenau an der Fundstelle. Was du nicht sicher prüfen kannst, markierst du mit „⚠ nicht geprüft“.
 
---
 
## Schritt 2 – Fragebogenerstellung
Jede Angabe im Fragebogen stammt aus Schritt 1 (im Folgenden „Inventar“). Was nicht im Inventar steht, kommt nicht vor. Du verwendest nur Quellen, die in 1b ausgewählt sind und ein Vollinventar haben.
 
### 2.1 Konstrukte
- **Auswahl:** Übernimm die Auswahl aus 1b unverändert. Verworfene Alternativen sind die in 1b verworfenen Quellen mit ihren Belegzitaten, keine Teilkonstrukte derselben Quelle.
- **Bezeichnung:** Theorie bzw. Instrument benennst du genau wie im Inventar.
- **Definition:**
  - Wörtlich aus C1, in Anführungszeichen mit Seite; Auslassungen mit […].
  - Fehlt sie: „Definition nicht in den Quellen enthalten; Operationalisierung: …“ (wörtlich aus C2).
  - Instruktionstexte, Itemformulierungen, Faktorbezeichnungen und Modellannahmen sind keine Definitionen.
- **Sekundärzitate:** „Autor (Jahr, zit. n. Quelle)“, nur wenn C1 die Zuschreibung im Literaturverzeichnis der Quelle nachweist. Passt der Titel nicht zum Konstrukt, ordne das Konstrukt der Quelle selbst zu und vermerke die Unstimmigkeit mit [eigene Bewertung].
- **Validierter Umfang:**
  - Verwende nur Konstrukte bzw. Subskalen aus dem finalen Modell der Quelle.
  - Ein Ausschluss aus C4 gilt nur für das dort genannte Konstrukt (Regel 4). Steht dort „Bezug nicht genannt“, wendest du ihn nicht an und führst ihn unter „Offene Punkte“ auf.
  - Ging ein Konstrukt nur als Einzelindikator ein, weise es als „als Skala nicht validiert“ aus.
- **Messverfahren (C3):** Übernimm es vollständig, wenn Items davon abhängen (Filter- oder Häufigkeitsfragen, Szenario, Technologiebeschreibung, Itemstamm). Filteritems kommen mit Antwortformat und Filterregel in Tabelle B. Ist die Filterregel mehrdeutig (z. B. eine Schwelle bei mehreren Items je Bereich), legst du die Verdichtung als [eigene Bewertung] fest.
- **Aggregation:**
  - Bildet die Quelle ein Konstrukt über Teilbereiche (z. B. Mittelwert über alle relevanten Aufgabenarten), übernimm die Aggregation mit **allen** Teilbereichen der Quelle.
  - Eine Teilauswahl ist nur zulässig, wenn ein Belegzitat genau diese Teilauswahl für genau dieses Konstrukt nennt.
  - Prüfe für jedes Einsatzfeld aus den Fall-Parametern, welcher Teilbereich es abdeckt. Deckt keiner es ab, gilt Regel 9.
 
### 2.2 Items
- **Anzahl:** Je Konstrukt 3–4 Originalitems; hat die Quelle weniger, alle. Kein Konstrukt (auch kein Kriterium) wird mit nur einem Item gemessen, wenn die Quelle mehr enthält. Begründe die Itemauswahl in „Adaption“.
- **Item-ID:** Lege das Schema einmal fest und stelle es Tabelle B voran:
  - aus dem Katalog: Katalogpräfix + Fragebogen-Nr. + Originalbezeichnung;
  - direkt aus einer Quelle: Quellenpräfix + Originalnummer;
  - ohne Nummer: Präfix + Konstruktname + Position.
- **Originalitem:**
  - zeichengenau aus C2, aus genau einer Quellenversion, mit Fundstelle;
  - liegt eine deutsche Originalfassung vor, ist sie der Ausgangspunkt (kein Ü);
  - eine eigene Übersetzung dokumentierst du mit Verfahren (z. B. Rückübersetzung) und weist sie als nicht validiert aus;
  - bei „⚠ Abweichung“: beide Fassungen nennen, Wahl mit [eigene Bewertung] begründen, Pretest-Prüfpunkt angeben.
- **Erlaubte Änderungen:** Technologiename, Pronomen/Genus, Modus, Auflösung doppelter Verneinungen. Jede andere Änderung ist I und braucht ein Belegzitat zur Definition.
- **Adaptionscodes:** Ü = Übersetzung, K = Kontext, I = Inhalt, S = Skala/Antwortformat.
  - Dokumentiere jede Änderung am Wortlaut, auch Streichungen und einzelne Wörter. Der Kerninhalt bleibt erhalten (z. B. „ohne Kontrolle“ bei Trust).
  - Ersetze unpassende Inhalte (z. B. Bezugspersonen) nicht durch eigene. Behalte das Item, kennzeichne die eingeschränkte Passung mit [eigene Bewertung] und nenne einen Pretest-Prüfpunkt.
  - Einen Ebenen- oder Perspektivwechsel („wir“ → „ich“) nimmst du nur vor, wenn das Item für die Zielgruppe sonst unbeantwortbar ist (Regel 8). Kennzeichne ihn als I (nicht validiert) und weise jede Hypothese mit diesem Konstrukt als explorativ aus.
  - „Unverändert“ steht nur, wenn Wortlaut und Antwortformat dem Original entsprechen.
- **Modus:**
  - Absichten, aktuelles Wissen und Einstellungen bleiben im Indikativ.
  - Konjunktiv nur, wo das Item eine Nutzung oder eine dabei entstehende Bewertung bzw. Emotion voraussetzt.
  - Ein Futur im Original bleibt Futur.
  - Innerhalb einer Skala gilt dieselbe Regel für alle Items. Bei Mischmodus entscheidet Regel 8; dokumentiere die Abweichung als K.
- **Allgemeine Instrumente:** Für „KI allgemein“ validierte Items bleiben allgemein. Eine Verengung auf die Fall-Technologie ist eine nicht validierte Adaption und muss begründet werden.
- **Eindimensionalität und Wortwahl:**
  - Füge keine Begriffe, Gegenstände, Bedingungen, Abschwächer oder Verstärker hinzu.
  - Löse doppelte Verneinungen und mehrdeutige Negationen auf, ohne die Intensität zu verändern (nicht „keine Bedenken“ → „ich bin sicher“). Kennzeichne das als I.
  - Verwende bei Ü und K keinen Begriff, der bereits in Items eines anderen Konstrukts vorkommt.
  - Begriffspaare, Beispielaufzählungen, Verstärker, gekoppelte Bedingungen und mehrdeutige Begriffe aus dem Original bleiben erhalten. Prüffrage: Nennt C4 für die Skala dieses Items einen Kennwert? Ja → Kennwert mit Seite in „Adaption“ zitieren. Nein → inhaltliches Belegzitat + Pretest-Prüfpunkt. Bei Mehrdeutigkeit immer ein Pretest-Prüfpunkt.
- **Polung (R):**
  - Nur, wenn die Quelle die Umpolung belegt oder das Item der Konstruktrichtung inhaltlich widerspricht. Ohne Beleg: [eigene Bewertung], auch bei jeder Hypothese mit diesen Items.
  - Items eines eigenständigen Faktors (z. B. Fear) sind innerhalb ihrer Skala nicht invers.
  - Sind alle Items einer validierten Skala gleich gepolt, bleibt der Wortlaut; Zustimmungstendenz wird Pretest-Prüfpunkt.
- **Auswertung:** Jede Skala getrennt; keine Skalen verschiedener Faktoren oder Quellen zusammenfassen.
 
### 2.3 Hypothesen
- Nur Hypothesen aus C5, die die Quelle empirisch geprüft hat. Je Prädiktorkonstrukt eine Hypothese mit einem Kriterium.
- Nenne H-Nr., Seite, Ergebnis (bestätigt / nicht bestätigt) und das wörtliche Belegzitat.
- Vermerke, wenn das Ergebnis aus einem Modell mit weiteren, hier nicht erhobenen Prädiktoren stammt oder ein Konstrukt anders gebildet wird als in der Quelle.
- Prädiktor und Kriterium stammen aus derselben Quelle und werden mit mindestens 3 Items gemessen (bzw. allen). Fehlt das Kriterium, nimm seine Items auf oder lass die Hypothese weg.
- Verwende den Konstruktnamen aus Tabelle A.
- Gegenannahme nur mit empirischem Beleg der Quelle (Zitat, Seite). Verallgemeinere sie nicht über die untersuchten Gruppen oder Bedingungen hinaus. Ohne Beleg: [eigene Bewertung].
 
### 2.4 Instruktion
- Anonymitätshinweis, vor dem ersten technologiebezogenen Item.
- **Technologiebeschreibung** [Modellwissen]:
  - nur die Einsatzfelder aus den Fall-Parametern;
  - Funktionen mit Modalverben („kann …“);
  - kein Nutzerverhalten und keine Kontrollpraxis als gegeben (kein „Ergebnisse werden geprüft“);
  - keine Vorteile, keine Wertungen.
- Gibt die Quelle ein Szenario oder einen Itemstamm vor, übernimm ihn an der entsprechenden Stelle.
- Die Instruktion nennt keine Filterregeln, Hypothesen oder Auswertungslogik.
- Hinweise auf Antwortoptionen (z. B. „kann ich nicht beurteilen“) gelten nur für die Blöcke, die diese Option haben; benenne diese Blöcke.
 
### 2.5 Skala
- **Standard:** 1–5 (stimme überhaupt nicht zu … stimme voll zu) + „kann ich nicht beurteilen“ (= fehlender Wert).
- **Abweichende Originalskala (C3):**
  - Begründet die Quelle ihre Skala inhaltlich und wird das Instrument getrennt ausgewertet: Originalskala behalten; nur die Zusatzoption als S kennzeichnen.
  - Sonst: auf 1–5 umstellen; Originalskala, Seite und Umstellungsgrund in Tabelle A; jedes betroffene Item als S.
  - Als Begründung aus der Quelle zählt nur ein Zitat, das andere Skalierungen ausdrücklich für geeignet erklärt. Ein Hinweis, andere Skalierungen „zu prüfen“, genügt nicht. Ohne solches Zitat: eigener Grund mit [eigene Bewertung] + Pretest-Prüfpunkt zur Reliabilität.
  - Jede geänderte Skala als nicht validiert ausweisen. Fehlt die Originalskala im Inventar: „nicht in den Quellen enthalten“.
- **Anderer Urteilstyp** (z. B. Fähigkeitseinschätzung → Zustimmung): als nicht validiert ausweisen.
- **Filter- und Häufigkeitsfragen** behalten ihr Originalformat.
 
---
 
## Typische Fehler (nicht wiederholen)
- ✗ Ausschluss von Indikatoren eines Prädiktors (TC) als Begründung für gekürzte Fit-Items (TTF) verwendet.
- ✗ „Die Autor:innen empfehlen, andere Skalierungen zu prüfen“ als Begründung für 5 statt 11 Stufen.
- ✗ Instruktion: „nur für Aufgabenarten, die Sie mindestens monatlich ausführen“.
- ✗ Technologiebeschreibung: „Die Ergebnisse werden von den Nutzer:innen geprüft“.
- ✗ Faktor „Acceptance“ umbenannt in „Vertrauen und Nutzenerwartung“.
- ✗ Heftnummer bzw. Autor:innen aus Vorwissen ergänzt oder weggelassen.
- ✗ Tabelle D „erfüllt“, obwohl Tabelle B eine Abweichung dokumentiert.
- ✗ Itemzahl geschätzt statt gezählt.
 
---
 
## Prüfung vor der Ausgabe von Schritt 2
Prüfe jede Zeile von Tabelle A–C erneut am Inventar bzw. an der Quelle, nicht aus dem Gedächtnis.
 
| Prüfpunkt | Regel |
|---|---|
| Jede Angabe stammt aus dem Inventar; keine Fakten aus Vorwissen | 1, 2 |
| Jede Entscheidung hat ein wörtliches Belegzitat, das das betroffene Konstrukt ausdrücklich nennt | 3, 4 |
| Eine Theorie je Konstrukt und Hypothese; Name nach Regel 6; Bezugsebene unverändert oder als I gekennzeichnet | 5–7 |
| 3–4 Items je Konstrukt (bzw. alle); Filteritems, Filterregel und Aggregation mit allen Teilbereichen; jedes Einsatzfeld abgedeckt oder unter „Offene Punkte“ | 2.1, 2.2, 9 |
| Items nicht zweidimensional, suggestiv oder mehrdeutig verneint; keine vorausgesetzte Erfahrung oder Entscheidungsbefugnis; Modus je Skala einheitlich | 8, 2.2 |
| Nur erlaubte Änderungen oder I mit Belegzitat; keine Intensitätsänderung; kein Begriff in Items verschiedener Konstrukte; jede Ü/K/I/S-Änderung dokumentiert | 2.2 |
| Instruktion: Anonymitätshinweis; Beschreibung mit Modalverben, ohne Praxis oder Vorteile; keine Filterregeln, Hypothesen, Auswertungslogik; Optionshinweise passen zu den Blöcken | 2.4 |
| Skala nach 2.5 behalten oder umgestellt und begründet; geänderte Skalen als nicht validiert ausgewiesen | 2.5 |
| Hypothesen: Prädiktor und Kriterium gemessen; Belegzitat; Modellabweichungen vermerkt; Gegenannahme belegt oder gekennzeichnet; explorative Hypothesen markiert | 2.3 |
| Itemzahlen durch Zählen der Zeilen von Tabelle B; Tabellen widersprechen sich nicht; keine Pauschalaussagen (z. B. „vollständig validiert“) | Konsistenz |
| Literatur nur aus 1a; vollständige Autorenliste; im Text ab drei Autor:innen „et al.“; fehlende Angaben als „nicht in den Quellen enthalten“ | 1, 2 |
 
**Status in Tabelle D:**
- „erfüllt“ nur mit Nachweis (Belegzitat oder Item-ID);
- „korrigiert“ mit Angabe, was geändert wurde;
- „Abweichung dokumentiert“ bei bewusster Abweichung von der Quelle;
- „nicht prüfbar“, wenn kein Nachweis möglich ist.
 
Korrigiere Verstöße, bevor du ausgibst.
 
---
 
## Ausgabe
**Teil I – Inventar (Schritt 1)**
1. 1a Formatanalyse
2. 1b Auswahl
3. 1c Vollinventar (C1–C5 je ausgewählter Quelle)
4. Liste aller ⚠-Markierungen
 
**Teil II – Fragebogen (Schritt 2)**
1. **Instruktion** (Anonymitätshinweis, neutrale Technologiebeschreibung)
2. **Tabelle A – Auswahl:** Theorie/Instrument | Konstrukt (Originalname) | Definition laut Quelle (Seite) | Quelle | Originalskala (Seite) | Passung zum Fall | Belegzitat (wörtlich, Seite) | verworfene Alternativen
3. **Tabelle B – Fragebogen** (gruppiert nach Theorie; ID-Schema davor): Item-ID | Konstrukt | Originalitem (Fundstelle) | finales Item | Adaption (Code + Begründung) | (R)
4. **Tabelle C – Hypothesen:** H | Hypothese | Gegenannahme | Prädiktor-Items | Kriterium-Items | Quelle (H-Nr., Seite, Ergebnis) | Belegzitat (wörtlich)
5. **Tabelle D – Prüfprotokoll:** Prüfpunkt | Status | Nachweis | betroffene Item-IDs bzw. H
6. **Offene Punkte** (nicht erfüllbare Vorgaben mit Grund; „keine“, wenn leer)
7. **Literaturverzeichnis nach APA 7:** alle direkt zitierten Quellen, auch die verworfenen, ausschließlich mit Angaben aus 1a. Sekundär zitierte Werke („zit. n.“) nur im Text.
 
Weitere Abschnitte (z. B. Auswertung, Pretest-Prüfpunkte) nur, wenn jede Aussage belegt oder gekennzeichnet ist und den Tabellen nicht widerspricht.
