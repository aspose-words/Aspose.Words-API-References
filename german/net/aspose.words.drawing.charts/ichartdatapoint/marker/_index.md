---
title: IChartDataPoint.Marker
linktitle: Marker
articleTitle: Marker
second_title: Aspose.Words für .NET
description: IChartDataPoint Marker eigendom. Gibt einen Datenmarker an. Marker wird bei Anforderung automatisch erstellt in C#.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/ichartdatapoint/marker/
---
## IChartDataPoint.Marker property

Gibt einen Datenmarker an. Marker wird bei Anforderung automatisch erstellt.

```csharp
public ChartMarker Marker { get; }
```

## Beispiele

Zeigt, wie mit Datenpunkten in einem Liniendiagramm gearbeitet wird.

```csharp
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

    // Betonen Sie die Datenpunkte des Diagramms, indem Sie sie als Rautenformen erscheinen lassen.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Glätten Sie die Linie, die die erste Datenreihe darstellt.
    chart.Series[0].Smooth = true;

    // Stellen Sie sicher, dass die Farben der Datenpunkte für die erste Serie nicht invertiert werden, wenn der Wert negativ ist.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Für ein übersichtlicheres Diagramm können wir das Format einzeln löschen.
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

* class [ChartMarker](../../chartmarker/)
* interface [IChartDataPoint](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
