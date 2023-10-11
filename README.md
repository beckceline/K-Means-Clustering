# K-Means-Clustering
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/beckceline/K-Means-Clustering/HEAD)

Für dieses Projekt werden wir versuchen K Means Clustering zu verwenden, um Universitäten in den USA in zwei Gruppen zu unterteilen: private und öffentliche.
Ein wichtiger Hinweis: Für diese Universitäten wissen wir die tatsächliche Zuordnung und finden sie im Datensatz. Wir werden sie aber ignorieren, da K Means Clustering ein Unsupervised Learning Algorithmus ist.
Normalerweise verwendet man den K Means Clustering Algorithmus für Daten, deren Zugehörigkeit zu einem Cluster man nicht kennt. In diesem Fall verwenden wir die Zuteilung, um beurteilen zu können, wie gut der Algorithmus performt. Da das in echten Anwendungen nicht möglich ist, sind Confusion Matrix und Classification Report am Ende des Projekts nur theoretische Auswertungen.

Wir verwenden einen DataFrame mit 770 Beobachtungen und den folgenden 18 Variablen:

* Private: Dummy Varaible mit "Yes" für private und "No" für öffentliche Einrichtungen
* Apps: Anzahl an erhaltenen Bewerbungen
* Accept: Anzahl an angenommenen Bewerbungen
* Enroll: Anzahl neu eingeschriebener Studenten
* Top10perc: Prozent der neuen Studenten der Top 10% einer High School Klasse
* Top25perc: Prozent der neuen Studenten der Top 25% einer High School Klasse
* F.Undergrad: Anzahl an Vollzeitstudenten
* P.Undergrad: Anzahl an Teilzeitstudenten
* Outstate: Gebühr für Studenten, die aus einem anderen Staat kommen
* Room.Board: Kosten für Räume und Mitarbeiter
* Books: Geschätze Kosten für Bücher
* Personal: Geschätzte persönliche Ausgaben
* PhD: Prozent der Fakultäten mit Ph.D.'s
* Terminal: Prozent der Fakultäten mit Terminal Degree
* S.F.Ratio: Rate der Studenten pro Fakultät
* perc.alumni: Prozent der Alumni die spenden
* Expend: Verwaltungskosten pro Student
* Grad.Rate: Abschlussrate

### Schritte

1. Importieren der Libraries: Wir beginnen mit dem Importieren der Python-Bibliotheken, die für die Datenanalyse und Visualisierung benötigt werden.

2. Daten einlesen: Der Datensatz wird aus einer Datei namens 'College_Data' eingelesen und in einen DataFrame 'df' geladen.

3. Datenüberblick: Wir werfen einen Blick auf die ersten Zeilen des DataFrames und verwenden die Funktionen 'info()' und 'describe()', um grundlegende Informationen über die Daten zu erhalten.

4. Explorative Datenanalyse: Wir erstellen Scatterplots und Histogramme, um Beziehungen zwischen den Merkmalen zu visualisieren. Dabei verwenden wir die "Private"-Spalte zur Färbung der Punkte.

5. K-Means-Cluster erstellen: Wir importieren die KMeans-Klasse aus der scikit-learn-Bibliothek und erstellen ein K-Means-Modell mit 2 Clustern. Das Modell wird auf die Daten angewendet, wobei die "Private"-Spalte entfernt wird.

6. Auswertung: Wir erstellen eine neue Spalte namens "Cluster", die 1 für private Universitäten und 0 für öffentliche Universitäten enthält. Anschließend erstellen wir eine Confusion Matrix und einen Classification Report, um die Leistung des K-Means-Clustering-Algorithmus zu bewerten.

### Ergebnis

Die Confusion Matrix zeigt:
* Für die Klasse "0" (öffentliche Universitäten) wurden 138 Universitäten korrekt zugeordnet, während 74 fälschlicherweise der Klasse "1" zugeordnet wurden.
* Für die Klasse "1" (private Universitäten) wurden 34 Universitäten korrekt zugeordnet, während 531 fälschlicherweise der Klasse "0" zugeordnet wurden.

Der Classification Report zeigt:
* Die Precision für Klasse "0" beträgt 0,21, während die Recall 0,65 beträgt. Der F1-Score liegt bei 0,31.
* Die Precision für Klasse "1" beträgt 0,31, während der Recall bei 0,06 liegt. Der F1-Score liegt bei 0,10.
Die Gesamtgenauigkeit des Modells beträgt 0,22.

Betrachtet man die Ergebnisse, zeigt sich, dass das K-Means-Clustering die Universitäten anhand der verfügbaren Merkmale in zwei Gruppen unterteilt hat. Die Genauigkeit ist zwar nicht sehr hoch, was angesichts der reinen Verwendung von Merkmalsdaten für das Clustering nicht überraschend ist. Dennoch ist es bemerkenswert, wie gut der Algorithmus ohne Kenntnis der tatsächlichen Zuordnung funktioniert hat.
Dieses Beispiel verdeutlicht, wie gut K-Means für die Gruppierung von Daten geeignet ist, insbesondere wenn keine vorherige Kenntnis über die tatsächlichen Zuordnungen vorliegt.

