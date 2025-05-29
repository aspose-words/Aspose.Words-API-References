---
title: IChartDataPoint Interface
linktitle: IChartDataPoint
articleTitle: IChartDataPoint
second_title: .NET için Aspose.Words
description: Ayrıntılı grafik veri noktası özellikleri için Aspose.Words.Drawing.Charts.IChartDataPoint arayüzünü keşfedin. Veri görselleştirmenizi zahmetsizce geliştirin!
type: docs
weight: 1220
url: /tr/net/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface

Grafikteki tek bir veri noktasının özelliklerini içerir.

```csharp
public interface IChartDataPoint
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/ichartdatapoint/bubble3d/) { get; set; } | Kabarcık grafiğindeki kabarcıklara 3 boyutlu efekt uygulanıp uygulanmayacağını belirtir. |
| [Explosion](../../aspose.words.drawing.charts/ichartdatapoint/explosion/) { get; set; } | Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif özelliğin ayarlanmadığı ve herhangi bir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca pasta grafikleri için geçerlidir. |
| [InvertIfNegative](../../aspose.words.drawing.charts/ichartdatapoint/invertifnegative/) { get; set; } | Değer negatifse üst öğenin renklerini tersine çevirip çevirmeyeceğini belirtir. |
| [Marker](../../aspose.words.drawing.charts/ichartdatapoint/marker/) { get; } | Bir veri işaretçisi belirtir. İşaretleyici, talep edildiğinde otomatik olarak oluşturulur. |

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
