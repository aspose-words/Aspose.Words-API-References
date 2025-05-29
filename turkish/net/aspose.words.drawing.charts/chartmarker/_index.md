---
title: ChartMarker Class
linktitle: ChartMarker
articleTitle: ChartMarker
second_title: .NET için Aspose.Words
description: Özelleştirilebilir işaretçilerle grafik veri görselleştirmenizi geliştirmek için başvuracağınız çözüm olan Aspose.Words.Drawing.Charts.ChartMarker sınıfını keşfedin.
type: docs
weight: 1040
url: /tr/net/aspose.words.drawing.charts/chartmarker/
---
## ChartMarker class

Bir grafik veri işaretçisini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartMarker
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Format](../../aspose.words.drawing.charts/chartmarker/format/) { get; } | Bu işaretleyicinin dolgu ve satır biçimlendirmesine erişim sağlar. |
| [Size](../../aspose.words.drawing.charts/chartmarker/size/) { get; set; } | Grafik işaretleyici boyutunu alır veya ayarlar. Varsayılan değer 7'dir. |
| [Symbol](../../aspose.words.drawing.charts/chartmarker/symbol/) { get; set; } | Grafik işaretleyici sembolünü alır veya ayarlar. |

## Örnekler

Bir çizgi grafiğinde veri noktalarıyla nasıl çalışılacağını gösterir.

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

    // Grafiğin veri noktalarını elmas şekilleri şeklinde göstererek vurgulayın.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // İlk veri serisini temsil eden çizgiyi düzeltin.
    chart.Series[0].Smooth = true;

    // İlk serinin veri noktalarının, değer negatif olduğunda renklerinin tersine dönmeyeceğini doğrulayın.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Daha temiz görünümlü bir grafik için formatı tek tek temizleyebiliriz.
    dataPoint.ClearFormat();

    // Ayrıca bir dizi veri noktasını aynı anda soyabiliriz.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Bir diziye belirli sayıda veri noktası uygular.
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
