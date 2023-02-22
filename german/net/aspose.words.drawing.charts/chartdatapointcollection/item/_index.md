---
title: ChartDataPointCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: ChartDataPointCollection eigendom. gibt zurückChartDataPoint für den angegebenen Index.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartdatapointcollection/item/
---
## ChartDataPointCollection indexer

gibt zurück[`ChartDataPoint`](../../chartdatapoint/) für den angegebenen Index.

```csharp
public ChartDataPoint this[int index] { get; }
```

### Beispiele

Zeigt, wie Sie mit Datenpunkten in einem Liniendiagramm arbeiten.

```csharp
[Test]
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Heben Sie die Datenpunkte des Diagramms hervor, indem Sie sie als Rautenformen erscheinen lassen.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Die Linie glätten, die die erste Datenreihe darstellt.
    chart.Series[0].Smooth = true;

    // Sicherstellen, dass Datenpunkte für die erste Serie ihre Farben nicht invertieren, wenn der Wert negativ ist.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Für ein sauberer aussehendes Diagramm können wir das Format individuell löschen.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Wir können auch eine ganze Reihe von Datenpunkten auf einmal entfernen.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Wendet eine Reihe von Datenpunkten auf eine Reihe an.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Siehe auch

* class [ChartDataPoint](../../chartdatapoint/)
* class [ChartDataPointCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartdatapointcollection/)
* Montage [Aspose.Words](../../../)


