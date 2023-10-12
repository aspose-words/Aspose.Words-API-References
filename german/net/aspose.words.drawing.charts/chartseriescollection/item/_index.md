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

Negative Indizes sind zulässig und zeigen den Zugriff von der Rückseite der Sammlung an. Beispielsweise bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird ein Nullverweis zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird ein Nullverweis zurückgegeben.

### Beispiele

Zeigt, wie man Reihendaten in einem Diagramm hinzufügt und entfernt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Säulendiagramm einfügen, das standardmäßig drei Serien von Demodaten enthält.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Jede Reihe hat vier Dezimalwerte: einen für jede der vier Kategorien.
// Vier Cluster mit drei Spalten stellen diese Daten dar.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Den Namen jeder Serie im Diagramm ausgeben.
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
// Dieses Diagramm enthält jetzt vier Cluster mit vier Spalten.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Eine Diagrammreihe kann auch wie folgt nach Index entfernt werden.
// Dadurch wird eine der drei Demoserien entfernt, die mit dem Diagramm geliefert wurden.
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


