---
title: ChartSeriesCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre Diagrammdaten mühelos mit der Methode „RemoveAt“ der ChartSeriesCollection – entfernen Sie schnell jede ChartSerie nach Index für eine optimierte Analyse.
type: docs
weight: 60
url: /de/net/aspose.words.drawing.charts/chartseriescollection/removeat/
---
## ChartSeriesCollection.RemoveAt method

Entfernt ein[`ChartSeries`](../../chartseries/) am angegebenen Index.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index der[`ChartSeries`](../../chartseries/) zu entfernen. |

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
