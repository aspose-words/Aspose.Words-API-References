---
title: Class ChartMarker
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.ChartMarker sınıf. Bir grafik veri işaretçisini temsil eder.
type: docs
weight: 750
url: /tr/net/aspose.words.drawing.charts/chartmarker/
---
## ChartMarker class

Bir grafik veri işaretçisini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartMarker
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Format](../../aspose.words.drawing.charts/chartmarker/format/) { get; } | Bu işaretleyicinin dolgu ve çizgi formatlamasına erişim sağlar. |
| [Size](../../aspose.words.drawing.charts/chartmarker/size/) { get; set; } | Grafik işaretleyici boyutunu alır veya ayarlar. Varsayılan değer 7. |
| [Symbol](../../aspose.words.drawing.charts/chartmarker/symbol/) { get; set; } | Grafik işaretleyici sembolünü alır veya ayarlar. |

### Örnekler

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


