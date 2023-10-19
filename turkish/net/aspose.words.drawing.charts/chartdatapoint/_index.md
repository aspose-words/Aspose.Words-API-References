---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartDataPoint sınıf. Grafikteki tek bir veri noktasının formatını belirtmeye izin verir C#'da.
type: docs
weight: 690
url: /tr/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Grafikteki tek bir veri noktasının formatını belirtmeye izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Kabarcık grafiğindeki baloncuklara 3 boyutlu efektin uygulanması gerekip gerekmediğini belirtir. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif, özelliğin ayarlanmadığı ve hiçbir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca Pasta grafikleri için geçerlidir. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Bu veri noktasının dolgu ve satır formatlamasına erişim sağlar. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Bu nesnenin biçimlendirmeyi uyguladığı veri noktasının dizini. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Değer negatifse ana öğenin renklerini ters çevirip çevirmeyeceğini belirtir. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Grafik veri işaretçisini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Bu veri noktasının biçimini temizler. Özellikler üst seride tanımlanan varsayılan değerlere ayarlanır. |

## Notlar

Bir seride,`ChartDataPoint` nesnenin bir üyesidir[`ChartDataPointCollection`](../chartdatapointcollection/) . [`ChartDataPointCollection`](../chartdatapointcollection/) içerir`ChartDataPoint` Her nokta için nesne.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
