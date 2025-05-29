---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: .NET için Aspose.Words
description: Tek tek grafik veri noktalarını kolayca biçimlendirmek ve veri görselleştirmenizi hassasiyetle geliştirmek için Aspose.Words.Drawing.Charts.ChartDataPoint sınıfını keşfedin.
type: docs
weight: 970
url: /tr/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Grafikteki tek bir veri noktasının biçimlendirmesini belirtmeye olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Kabarcık grafiğindeki kabarcıklara 3 boyutlu efekt uygulanıp uygulanmayacağını belirtir. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif özelliğin ayarlanmadığı ve herhangi bir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca pasta grafikleri için geçerlidir. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Bu veri noktasının dolgu ve satır biçimlendirmesine erişim sağlar. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Bu nesnenin biçimlendirmeyi uyguladığı veri noktasının dizini. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Değer negatifse üst öğenin renklerini tersine çevirip çevirmeyeceğini belirtir. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Grafik veri işaretçisini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Bu veri noktasının biçimini temizler. Özellikler, ana seride tanımlanan varsayılan değerlere ayarlanır. |

## Notlar

Bir dizide,`ChartDataPoint` nesne bir üyedir[`ChartDataPointCollection`](../chartdatapointcollection/) . [`ChartDataPointCollection`](../chartdatapointcollection/) bir içerir`ChartDataPoint` her nokta için nesne.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
