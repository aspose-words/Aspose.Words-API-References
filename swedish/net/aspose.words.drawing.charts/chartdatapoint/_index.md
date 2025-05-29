---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartDataPoint för att enkelt formatera enskilda diagramdatapunkter och förbättra din datavisualisering med precision.
type: docs
weight: 970
url: /sv/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Gör det möjligt att ange formatering för en enskild datapunkt i diagrammet.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Anger om bubblorna i bubbeldiagrammet ska ha en 3D-effekt. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Anger hur mycket datapunkten ska flyttas från cirkeldiagrammets mitt. Kan vara negativ, negativ betyder att egenskapen inte är angiven och ingen explosion ska tillämpas. Gäller endast cirkeldiagram. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering för denna datapunkt. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Index för datapunkten som detta objekt formaterar. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Anger om förälderelementet ska invertera sina färger om värdet är negativt. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Anger diagramdatamarkör. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Rensar formatet för denna datapunkt. Egenskaperna ställs in på standardvärdena som definierats i den överordnade serien. |

## Anmärkningar

På en serie, den`ChartDataPoint` objektet är medlem i[`ChartDataPointCollection`](../chartdatapointcollection/) . Den[`ChartDataPointCollection`](../chartdatapointcollection/) innehåller en`ChartDataPoint` objekt för varje punkt.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
