---
title: ChartDataPointCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: ChartDataPointCollection Count mülk. Sayıyı döndürürChartDataPoint bu koleksiyonda C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartdatapointcollection/count/
---
## ChartDataPointCollection.Count property

Sayıyı döndürür[`ChartDataPoint`](../../chartdatapoint/) bu koleksiyonda.

```csharp
public int Count { get; }
```

## Örnekler

Çizgi grafikte veri noktalarıyla nasıl çalışılacağını gösterir.

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

    // Grafiğin veri noktalarını baklava şekilleri şeklinde göstererek vurgulayın.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // İlk veri serisini temsil eden çizgiyi düzeltin.
    chart.Series[0].Smooth = true;

    // Değer negatifse, ilk serinin veri noktalarının renklerini tersine çevirmeyeceğini doğrulayın.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Daha temiz görünen bir grafik için formatı tek tek temizleyebiliriz.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Ayrıca bir dizi veri noktasının tamamını aynı anda kaldırabiliriz.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Bir diziye bir dizi veri noktası uygular.
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

### Ayrıca bakınız

* class [ChartDataPointCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
