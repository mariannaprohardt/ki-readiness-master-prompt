# ki-readiness-master-promt
Das KI-Readiness Master Promt von Marianna Prohardt im Rahmen des Praxismoduls im CMP Studium WINGS
## Ziele des Artefakts

Der Master-Prompt soll ein großes Sprachmodell (NotebookLM) so anleiten, dass es aus der bereitgestellten Datenbasis und den Unterlagen automatisiert einen Fragebogen zur Messung der KI-Readiness von Mitarbeitenden erstellt.

### Inhaltliche Ziele
1. **Theoriebasierung:** Das Modell schlägt eine oder mehrere geeignete Theorien vor und begründet deren Auswahl für den Anwendungsfall KI-Readiness.
2. **Theoretische Herleitung:** Jedes Item wird nachvollziehbar aus einem Konstrukt der gewählten Theorie abgeleitet.
3. **Theorietrennung:** Items und Konstrukte unterschiedlicher Theorien werden nicht vermischt.
4. **Hypothesenableitung:** Das Modell leitet aus Theorie und Studien begründete Hypothesen zu den Wirkzusammenhängen ab.
5. **Quellenbindung:** Die bereitgestellten Unterlagen bilden die primäre Grundlage; ergänzendes Modellwissen wird kenntlich gemacht.

### Methodische Ziele (Itemqualität)
6. **Eindimensionalität:** Jedes Item erfasst genau einen Aspekt (keine Double-Barreled-Questions).
7. **Neutralität:** Items sind nicht suggestiv formuliert.
8. **Einheitliches Antwortformat:** Alle Items verwenden eine konsistente Skala (z. B. 5- oder 7-stufige Likert-Skala).
9. **Transparenz:** Der Fragebogen enthält eine Zuordnungstabelle Theorie → Konstrukt → Item → Quelle.

### Anwendungsbezogene Ziele
10. **Praxistauglichkeit:** Der Fragebogen ist ohne Methodenkenntnisse im Unternehmen einsetzbar.
11. **Reproduzierbarkeit:** Der Master-Prompt erzeugt bei erneuter Ausführung inhaltlich vergleichbare Ergebnisse.

### Evaluationsmaßstab
Die Erreichung der Ziele 3, 6, 7 und 9 wird je Version durch KI-Agenten geprüft (siehe `evaluation/`).
