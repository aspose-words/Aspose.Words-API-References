---
title: ChartDataPointCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Count i ChartDataPointCollection, som effektivt returnerar det totala antalet ChartDataPoints, vilket förbättrar din datavisualisering.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartdatapointcollection/count/
---
## ChartDataPointCollection.Count property

Returnerar antalet[`ChartDataPoint`](../../chartdatapoint/) i den här samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar hur man arbetar med datapunkter i ett linjediagram.

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

    // Betona diagrammets datapunkter genom att få dem att visas som diamantformer.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Jämna ut linjen som representerar den första dataserien.
    chart.Series[0].Smooth = true;

    // Verifiera att datapunkterna för den första serien inte inverterar sina färger om värdet är negativt.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // För en renare graf kan vi rensa formatet individuellt.
    dataPoint.ClearFormat();

    // Vi kan också ta bort en hel serie datapunkter samtidigt.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Tillämpar ett antal datapunkter på en serie.
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

### Se även

* class [ChartDataPointCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
