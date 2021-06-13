# EA 09 - Logistic Regression Exercise
### Data Science SS 21
### Christian Kitte 

### Exercise 1 von 2: Lineare Regression

Make up your own personal dataset and predict the regression curve.

#### Fiktiver Kontext:
An freien Mitarbeitern werden Aufträge vergeben, welche nach vorheriger Absprache von diesen zu erledigen sind. Es ist normal, dass es eine Reihe von Gründen gibt, warum diese nicht erfolgreich sind. Nicht immer sind diese von den Mitarbeitern zu vertreten. Ein Auftrag wurd erfolgreich erledigt, sofern er fristgerecht und korrekt zur weiteren Verwendung vorliegt. Um hier nach möglichen Zusammenhängen zu suchen, wurde die Zahl der zugeteilten sowie der Erledigten Aufträge notiert. Hierbei können natürlich nur Aufträge einer vergleichbaren Art zusammen ausgewertet werden (beispielsweise nur im gleichen Bereich oder gleicher Zielgruppe).

Die [**hier vorliegende CSV Datei Auftraege.csv**](https://github.com/ChristianKitte/HelloRegression/blob/main/Auftraege.csv) enthält die fiktive Anzahl von vergebenen Aufträgen und die Anzahl der hiervon erfolgreich durchgeführten. Hierbei wurden die Zahlen bereinigt, so dass nur die tatsächlich zu realisierenden Aufträge Berücksichtigung finden. Dieser Schritt müsste in einem realen Umfeld besondere Beachtung finden. 

Die Daten sind auf GitHub als CSV Datei verfügbar (Link siehe unten).

Mit Hilfe der linearen Regression soll versucht werden, einen möglichen Zusammenhang zu erkennen. Problematisch können heirbei Outliner sein, welche den allgemeinen Trend entgegen laufen. Eine Steigerung hiervon währe, weitere Merkmale wie die Länge des Arbeitsverhältnisses zu berücksichtigen.

#### Ergebnis:
In der zum Schluss des [**Notebook**](https://github.com/ChristianKitte/HelloRegression/blob/main/Linear_Regression.ipynb) zu sehenden Ausgabe, sind die Grünen Punkte die zum Training verwendeten Daten, die Roten die vorhergesagten. Der Regressionsgraph ist in blau eingetragen.

Der Koeffizient kann zwischen 0 und 1 liegen und negativ sein. Hier beträgt er 0,7. Er ist positiv, daher der Anstieg der Geraden. In der Praxis bedeutet dies, dass es eine positive Relation gibt. Je mehr Aufträge erteilt wurden, umso höher war tendenziell die erfolgreiche Ausführung.

Der Wert 0,7 ist eher weniger gut, jedoch sind bei den Daten eine Reihe Ausreißer (dies kommt in der Praxis durchaus vor). Hier könnte durch mehr Daten oder aber dem Ausschluss der Ausreißer die Vorhersage verbessert werden.

Würde es sich bei näherer Betrachtung herausstellen, dass solche Ausreißer beispielsweise durch Ausscheiden des Mitarbeiter, einer Fehlerhaften Vergabe etc. verursacht würden, würden deren nicht Berücksichtigung das Ergebnis genauer machen.

Grundsätzlich entspricht der Graph dem erwarteten Ergebnis: In der Tendenz bedeuten mehr Aufträge mehr erfolgreiche Durchführungen. Die Streuung ist den bewust großen Schwankungen zuzurechnen.

### Exercise 2 von 2: Logistische Regression

You are walking in the forrest and see an iris and measure: 4.8,2.5,5.3,2.4.
Is this an Iris Virginica or not? 

Als Basis zur Bearbeitung dient das berühmte [**Iris flower data set**](https://en.wikipedia.org/wiki/Iris_flower_data_set).

#### Ergebnis:

Die komplette und ausführliche Lösung dieser Aufgabenstellung findet sich in diesem [**Notebook**](https://github.com/ChristianKitte/HelloRegression/blob/main/Logistische_Regression.ipynb). Bei der Bearbeitung zeigte sich, dass das Ergebnis auf Basis von Modellen, welche nur mit einem der vier Merkmalen traniert wurde, nicht eindeutig ist. Wird beispielsweise alleine Sepal Length zur Beurteilung herangezogen, so ist die Wahrscheinlichkeit eher sehr klein, dass es sich um eine Iris Virginica handelt. Nimmt man hingegen Petal Width, so ist die Wahrscheinlichkeit für das Gegenteil sehr hoch.

Daher wurde im zweiten Schritt ein Modell mit allen vier Merkmalen trainiert. Auf Basis eines mit allen vier features trainierten Modells erhalten wir die Aussage, dass es sich bei der Blume zu 97,6 % um eine Iris Virginica handelt.

Dem schließe ich mich an: Ja, es handelt sich um eine Iris Virginica !

#### Anmerkung:

Ein großer Teil des im Notebook für die zweite Aufgabe verwendeten Codes dient lediglich der Verdeutlichung, Visualisierung und sonstiger Ausgaben und kann grundsätzlich entfallen. Es ist hierbei erstaunlich, wie hilfreich eine Bibliothek wie sklearn sein kann. Wer sich primär nur für das Model auf Basis aller Features interessiert, findet dies am Ende des Notebooks :).

