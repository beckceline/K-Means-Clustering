# K-Means-Clustering
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/beckceline/K-Means-Clustering/HEAD)

Für dieses Projekt werden wir versuchen K Means Clustering zu verwenden, um Universitäten in den USA in zwei Gruppen zu unterteilen: Private und öffentliche.

Ein wichtiger Hinweis gleich zu beginn: Für diese Universitäten wissen wir die tatsächliche Zuordnung und finden sie im Datensatz. Wir werden sie aber ignorieren da K Means Clustering ein Unsupervised Learning Algorithmus ist.

Normalerweise verwendet man den K Means Clustering Algorithmus für Daten, deren Zugehörigkeit zu einem Cluster man nicht kennt. In diesem Fall verwenden wir die Zuteilung, um beurteilen zu können, wie gut der Algorithmus performt. Da das in echten Anwendungen nicht möglich ist sind Confusion Matrix und Classification Report am Ende des Projekts nur theoretische Auswertungen.

Die Daten

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

Schritte

1. Importieren der Libraries: Wir beginnen mit dem Importieren der Python-Bibliotheken, die für die Datenanalyse und Visualisierung benötigt werden.

2. Daten einlesen:Der Datensatz wird aus einer Datei namens 'College_Data' eingelesen und in einen DataFrame 'df' geladen.

3. Datenüberblick: Wir werfen einen Blick auf die ersten Zeilen des DataFrames und verwenden die Funktionen 'info()' und 'describe()', um grundlegende Informationen über die Daten zu erhalten.

4. Explorative Datenanalyse: Wir erstellen Scatterplots und Histogramme, um Beziehungen zwischen den Merkmalen zu visualisieren. Dabei verwenden wir die "Private"-Spalte zur Färbung der Punkte.

5. K-Means-Cluster erstellen: Wir importieren die KMeans-Klasse aus der scikit-learn-Bibliothek und erstellen ein K-Means-Modell mit 2 Clustern. Das Modell wird auf die Daten angewendet, wobei die "Private"-Spalte entfernt wird.

6. Auswertung: Wir erstellen eine neue Spalte namens "Cluster", die 1 für private Universitäten und 0 für öffentliche Universitäten enthält. Anschließend erstellen wir eine Confusion Matrix und einen Classification Report, um die Leistung des K-Means-Clustering-Algorithmus zu bewerten.

Ergebnis

Die Auswertung des K-Means-Clustering-Algorithmus zeigt, dass die Zuordnung der Universitäten zu den Clustern relativ gut funktioniert, obwohl der Algorithmus nur die reinen Eigenschaften der Universitäten verwendet. Die Ergebnisse könnten in realen Anwendungen weiter untersucht werden, um fundierte Schlussfolgerungen zu ziehen.

