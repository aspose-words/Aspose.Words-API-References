---
title: ChartDataPoint.Index
second_title: Aspose.Words for .NET API Referansı
description: ChartDataPoint mülk. Bu nesnenin biçimlendirmeyi uyguladığı veri noktasının dizini.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartdatapoint/index/
---
## ChartDataPoint.Index property

Bu nesnenin biçimlendirmeyi uyguladığı veri noktasının dizini.

```csharp
public int Index { get; }
```

### Örnekler

Çizgi grafikte veri noktalarıyla nasıl çalışılacağını gösterir.

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

    // Grafiğin veri noktalarını elmas şekiller olarak göstererek vurgulayın.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // İlk veri serisini temsil eden satırı düzeltin.
    chart.Series[0].Smooth = true;

    // Değer negatifse, ilk seri için veri noktalarının renklerini tersine çevirmediğini doğrulayın.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Daha temiz bir grafik için formatı tek tek temizleyebiliriz.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Aynı anda bir dizi veri noktasının tamamını da ayıklayabiliriz.
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

* class [ChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartdatapoint/)
* toplantı [Aspose.Words](../../../)


