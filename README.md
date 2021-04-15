# Experimente

## NSGA2-ALPS mit verschiedenen Parametern

### Verschiedene ALPS-spezifische Parameter
Die folgenden Fragen sollen mit den Experimenten beantwortet werden:
- Wie wirken sich die Elemente von ALPS auf die Pareto-Front aus? (Schichten-Anzahl, Alterungs-Schema, Mating-Pool-Größe)
- Der Algorithmus sollte in den folgenden Szenarien theoretisch gute/schlechte Ergebnisse liefern. Es soll herausgefunden werden ob dies tatsächlich der Fall ist.
  - Kleine Populationen sollen trotz ihrer Größe nicht verfrüht Konvergieren, da in der untersten Schicht regelmäßig neues Genmaterial in die Population eingefügt wird.
  - Die gesammte Pareto Front sollte auch mit einer kleinen Population gut abgedeckt werden nach einer ausreichenden Anzahl an Generationen.
  - Auch bei einfachen Problemen sollte die Population zur Pareto-Front langsam konvergieren. (Je weniger Generationen, desto besser sollte NSGA2 im Vergleich zu ALPS-NSGA2 werden.)
  - Je mehr Schichten verwendet werden desto geringer kann die Alterslücke sein und je weniger Schichten, desto höher muss die Alterslücke sein.
  - Die älteste Schicht profitiert auch von der vorletzten, wenn von dieser keine Lösungen explizit in die nächste Schicht aufsteigen können, solange bei der Kreuzung neues Genmaterial der vorletzten Schicht verwendet wird und dadurch die Diversität erhält.
  - Mit wenigen Schichten und einer kleinen Alterslücke, dient die vorletzte Schicht nur zum erhalten der Diversität und die Lösungen in der obersten Schicht entwickeln sich ähnlich zum klassischen NSGA-II. (Die Konvergenz wird eingeschränkt aber nicht so stark als wenn Lösungen auch in die oberste Schicht aufsteigen.)
- Wie steigt genetisches Material in den Schichten auf?
- Für welche Art von Problemen ist der NSGA2-ALPS geeignet?
- Für welche Art von Problemen ist der NSGA2-ALPS **nicht** geeignet?
  (Ist der Algorithmus geeignet für Probleme mit vielen nicht verbundenen/konvexen/nicht-konvexen/etc. Pareto-Fronten?)

Es werden die folgenden Paramereinstellungen getestet:
[TODO]

Es werden verschiedene Probleme ausgewählt, die je eine spezifische schwierige Eigenschaft aufweisen sollen.
- Probleme: ZDT, DTLZ
- Problemgröße: verschieden je nach Problem


## Vergleiche mit anderen Algorithmen
### Parameter
[TODO]

ALPS-Parameter: (je nachdem welche Parameter in vorherigen Experimenten die besten Hypervolumen erzielt haben)
- Alters-Schema: [TODO] 
- Alters-Lücke: [TODO]
- Anzahl an Schichten: [TODO]

### NSGA-II
Die folgenden Fragen sollen mit den Experimenten beantwortet werden:
- Wie wirken sich die Elemente von ALPS auf die Pareto-Front aus? (Schichten-Anzahl, Alterungs-Schema, Mating-Pool-Größe)
- Wird NSGA-II durch die neue Struktur der Population eingeschränkt und liefert dadurch schlechtere Ergebnisse?
- Ist die Spread/Spacing besser als bei NSGA-II?
- Auch bei einfachen Problemen sollte die Population zur Pareto-Front langsam konvergieren. (Je weniger Generationen, desto besser sollte NSGA2 im Vergleich zu ALPS-NSGA2 werden.)
- NSGA2-ALPS ohne Mutation sollte besser Diversität erhalten als NSGA2 ohne Mutation.