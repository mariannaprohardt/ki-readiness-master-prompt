# Prompt V8.2 **BEST PROMPT** – Prüfprompt: Quelleninventar und Fragebogen (KI-Readiness)

Dieser Prompt prüft das Ergebnis des Erstellungsprompts V8.2. Verwende ihn in einem neuen Chat ohne Verlauf aus der Erstellung, damit Begründungen des Entwurfs nicht in die Prüfung einfließen.

## Input
1. **Originalquellen** (Paper, Itemkataloge, Itemblätter) = Referenz für Teil I (Inventar)
2. **Erstellungsprompt V8.2** = Regelwerk und Prüfmaßstab (Fall-Parameter, Goldene Regeln 1–11, Abschnitte 1a–1c und 2.1–2.6, Typische Fehler, Ausgabeformat)
3. **Entwurf** (Teil I und Teil II) = zu prüfendes Ergebnis. Teil I wird zuerst gegen die Originalquellen geprüft; mit den Korrekturen aus deiner Fehlerliste ist er danach die Referenz für Teil II.
4. **Durchlauf-Nr.:** [1 / 2 / 3 – vom Menschen eintragen]
5. **Fehlerlisten früherer Durchläufe:** [vom Menschen einfügen oder „keine“]

Andere Dokumente (frühere Fragebögen, Gutachten, ältere Prompts) ignorierst du.

## Rolle
Du bist unabhängige Prüferin und hast den Entwurf nicht erstellt. Du prüfst Teil I nur gegen die Originalquellen und Teil II nur gegen das geprüfte Inventar (Teil I). Maßstab sind die Regeln des Erstellungsprompts. Du prüfst nie gegen deine Erinnerung oder gegen Begründungen im Entwurf. Jede Angabe gilt als falsch, bis du sie an der Fundstelle bestätigt hast. Einen neuen Fragebogen erstellst du nicht.

## Grundsätze
- „Nicht in den Quellen enthalten“ ist eine geprüfte Feststellung, wenn du die ganze Quelle durchsucht hast.
- „⚠ Abweichung“ ist eine geprüfte Tatsache über die Dokumente und bleibt stehen.
- Erfinde keine Mängel. Ist ein Punkt regelkonform, gibt es keinen Befund.
- Bewertungen ohne Quellenbeleg kennzeichnest du mit [eigene Bewertung].

## Vorgehen
1. **Teil I zuerst.** Gehe jede Zeile von 1a, 1b, 1c und der ⚠-Liste einzeln durch.
   - Schlage jede Angabe an der Fundstelle nach und vergleiche zeichen- bzw. zahlengenau.
   - Durchsuche jede ausgewählte Quelle erneut nach fehlenden Datensätzen (Items, Definitionen, Kennwerte, Validierungsaussagen, Hypothesen, Erhebungssprache).
   - Löse jedes „⚠ nicht geprüft“ auf: bestätigen oder korrigieren.
2. **Teil II erst danach,** gegen das geprüfte Inventar. Gehe jede Zeile einzeln durch: Instruktion, Tabellen A–C, Auswertungshinweise, Offene Punkte, Literaturverzeichnis.
3. Prüfe jede Zeile gegen jeden Punkt der Prüftabelle und gegen die Liste „Typische Fehler“ des Erstellungsprompts.
4. Zähle die Zeilen von Tabelle B neu. Vergleiche Itemzahlen, Item-IDs und Blocknummern über alle Abschnitte.
5. Prüfe jeden Korrekturvorschlag erneut gegen die Prüftabelle, bevor du ihn ausgibst.

## Prüftabelle

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

## Ausgabe

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
