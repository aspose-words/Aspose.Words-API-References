---
title: ChartSeriesCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: ChartSeriesCollection eigendom. Gibt a zurückChartSeries am angegebenen Index.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

Gibt a zurück[`ChartSeries`](../../chartseries/) am angegebenen Index.

```csharp
public ChartSeries this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index in die Sammlung. |

### Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff von der Rückseite der Sammlung an. Zum Beispiel bedeutet -1 das letzte Element, -2 bedeutet das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

### Beispiele

Zeigt, wie Reihendaten in einem Diagramm hinzugefügt und entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Säulendiagramm ein, das standardmäßig drei Reihen von Demodaten enthält.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Jede Reihe hat vier Dezimalwerte: einen für jede der vier Kategorien.
// Vier Cluster aus drei Spalten repräsentieren diese Daten.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Drucken Sie den Namen jeder Serie im Diagramm.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Dies sind die Namen der Kategorien im Diagramm.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Wir können eine Reihe mit neuen Werten für bestehende Kategorien hinzufügen.
// Dieses Diagramm enthält nun vier Cluster mit vier Spalten.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });

// Eine Chartserie kann auch per Index entfernt werden, wie hier.
// Dadurch wird eine der drei Demo-Serien entfernt, die mit dem Diagramm geliefert wurden.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));

// Mit dieser Methode können wir auch alle Daten des Diagramms auf einmal löschen.
// Beim Erstellen eines neuen Diagramms werden auf diese Weise alle Demodaten gelöscht
// bevor wir mit der Arbeit an einem leeren Diagramm beginnen können.
chartData.Clear();
```

### Siehe auch

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* Montage [Aspose.Words](../../../)


