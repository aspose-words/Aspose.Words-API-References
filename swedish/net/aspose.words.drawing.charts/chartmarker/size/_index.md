---
title: ChartMarker.Size
second_title: Aspose.Words för .NET API Referens
description: ChartMarker fast egendom. Hämtar eller ställer in diagrammarkörens storlek. Standardvärdet är 7.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartmarker/size/
---
## ChartMarker.Size property

Hämtar eller ställer in diagrammarkörens storlek. Standardvärdet är 7.

```csharp
public int Size { get; set; }
```

### Exempel

Visar hur man arbetar med datapunkter på ett linjediagram.

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

    // Framhäv diagrammets datapunkter genom att få dem att visas som diamantformer.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Jämna ut linjen som representerar den första dataserien.
    chart.Series[0].Smooth = true;

    // Kontrollera att datapunkter för den första serien inte kommer att invertera sina färger om värdet är negativt.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // För en renare graf kan vi rensa format individuellt.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Vi kan också ta bort en hel serie datapunkter på en gång.
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

* class [ChartMarker](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartmarker/)
* hopsättning [Aspose.Words](../../../)


