---
title: ChartDataPointCollection Class
linktitle: ChartDataPointCollection
articleTitle: ChartDataPointCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartDataPointCollection, din nyckel till att enkelt hantera ChartDataPoint-samlingar för förbättrad datavisualisering.
type: docs
weight: 980
url: /sv/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Representerar en samling av en[`ChartDataPoint`](../chartdatapoint/) .

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | Returnerar antalet[`ChartDataPoint`](../chartdatapoint/) i den här samlingen. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Returer[`ChartDataPoint`](../chartdatapoint/) för det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Rensar formatet för alla[`ChartDataPoint`](../chartdatapoint/) i den här samlingen. |
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(*int, int*) | Kopierar format från källdatapunkten till destinationsdatapunkten. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(*int*) | Hämtar en flagga som anger om datapunkten vid det angivna indexet har standardformat. |

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

* class [ChartDataPoint](../chartdatapoint/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
