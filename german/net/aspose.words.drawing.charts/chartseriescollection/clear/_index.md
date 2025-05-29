---
title: ChartSeriesCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: Löschen Sie mühelos alle ChartSeries aus Ihrer Sammlung mit der Methode ChartSeriesCollection Clear. Optimieren Sie noch heute Ihr Datenmanagement!
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/chartseriescollection/clear/
---
## ChartSeriesCollection.Clear method

Entfernt alle[`ChartSeries`](../../chartseries/) aus dieser Sammlung.

```csharp
public void Clear()
```

## Beispiele

Zeigt, wie man Reihendaten in einem Diagramm hinzufügt und entfernt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Säulendiagramm ein, das standardmäßig drei Reihen von Demodaten enthält.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Jede Reihe hat vier Dezimalwerte: einen für jede der vier Kategorien.
// Vier Cluster mit jeweils drei Spalten stellen diese Daten dar.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Drucken Sie den Namen jeder Reihe im Diagramm.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Dies sind die Namen der Kategorien im Diagramm.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Wir können eine Reihe mit neuen Werten für vorhandene Kategorien hinzufügen.
// Dieses Diagramm enthält jetzt vier Cluster mit jeweils vier Spalten.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Eine Diagrammreihe kann auch nach Index entfernt werden, wie folgt.
// Dadurch wird eine der drei Demoserien entfernt, die mit dem Diagramm geliefert wurden.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Mit dieser Methode können wir auch alle Daten des Diagramms auf einmal löschen.
// Beim Erstellen eines neuen Diagramms können auf diese Weise alle Demodaten gelöscht werden
// bevor wir mit der Arbeit an einem leeren Diagramm beginnen können.
chartData.Clear();
```

### Siehe auch

* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
