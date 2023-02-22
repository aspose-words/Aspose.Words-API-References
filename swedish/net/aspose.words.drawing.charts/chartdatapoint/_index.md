---
title: Class ChartDataPoint
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartDataPoint klass. Tillåter att ange formatering av en enskild datapunkt på diagrammet.
type: docs
weight: 650
url: /sv/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Tillåter att ange formatering av en enskild datapunkt på diagrammet.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } |  |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Ger tillgång till fyllnings- och linjeformatering av denna datapunkt. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Index för datapunkten som detta objekt tillämpar formatering på. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } |  |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } |  |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Rensar formatet för denna datapunkt. Egenskaperna är inställda på standardvärdena definierade i den överordnade serien. |

### Anmärkningar

På en serie`ChartDataPoint` objektet är medlem i[`ChartDataPointCollection`](../chartdatapointcollection/) . Den[`ChartDataPointCollection`](../chartdatapointcollection/) innehåller en`ChartDataPoint` objekt för varje punkt.

### Exempel

Visar hur man arbetar med datapunkter på ett linjediagram.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


