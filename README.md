# EA 09 - Logistic Regression Exercise
### Data Science SS 21
### Christian Kitte 

### Exercise 1: Lineare Regression

Make up your own personal dataset and predict the regression curve.

#### Fiktiver Kontext:
An freien Mitarbeitern werden Aufträge vergeben, welche nach vorheriger Absprache von diesen zu erledigen sind. Es ist normal, dass es eine Reihe von Gründen gibt, warum diese nicht erfolgreich sind. Nicht immer sind diese von den Mitarbeitern zu vertreten. Ein Auftrag wurd erfolgreich erledigt, sofern er fristgerecht und korrekt zur weiteren Verwendung vorliegt.

Die [**hier vorliegende CSV Datei Auftraege.csv**](https://github.com/ChristianKitte/HelloRegression/blob/main/Auftraege.csv) enthält die fiktiven Anzahl von vergebenen Aufträgen und die Anzahl der hiervon erfolgreich durchgeführten. Hierbei wurden die Zahlen bereinigt, so dass nur die tatsächlich zu realisierenden Aufträge Berücksichtigung finden. Dieser Schritt müsste in einem realen Umfeld besondere Beachtung finden. 

Mit Hilfe der linearen Regression soll versucht werden, einen möglichen Zusammenhang zu erkennen. Problematisch können heirbei Outliner sein, welche den allgemeinen Trend entgegen laufen. Eine Steigerung hiervon währe, weitere Merkmale wie die Länge des Arbeitsverhältnisses zu berücksichtigen.

#### Ergebnis:
In der zum Schluss des [**Notebook**](https://github.com/ChristianKitte/HelloRegression/blob/main/Linear_Regression.ipynb) zu sehenden Ausgabe, sind die Grünen Punkte die zum Training verwendeten Daten, die Roten die vorhergesagten. Der Regressionsgraph ist in blau eingetragen.

Der Koeffizient kann zwischen 0 und 1 liegen und negativ sein. Hier beträgt er 0,7. Er ist positiv, daher der Anstieg der Geraden. In der Praxis bedeutet dies, dass es eine positive Relation gibt. Je mehr Aufträge erteilt wurden, umso höher war tendenziell die erfolgreiche Ausführung.

Der Wert 0,7 ist eher weniger gut, jedoch sind bei den Daten eine Reihe Ausreißer (dies kommt in der Praxis durchaus vor). Hier könnte durch mehr Daten oder aber dem Ausschluss der Ausreißer die Vorhersage verbessert werden.

Würde es sich bei näherer Betrachtung herausstellen, dass solche Ausreißer beispielsweise durch Ausscheiden des Mitarbeiter, einer Fehlerhaften Vergabe etc. verursacht würden, würden deren nicht Berücksichtigung das Ergebnis genauer machen.

Grundsätzlich entspricht der Graph dem erwarteten Ergebnis: In der Tendenz bedeuten mehr Aufträge mehr erfolgreiche Durchführungen. Die Streuung ist den bewust großen Schwankungen zuzurechnen.
