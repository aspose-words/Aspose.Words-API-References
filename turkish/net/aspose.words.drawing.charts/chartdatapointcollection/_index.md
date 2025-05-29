---
title: ChartDataPointCollection Class
linktitle: ChartDataPointCollection
articleTitle: ChartDataPointCollection
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için ChartDataPoint koleksiyonlarını zahmetsizce yönetmenin anahtarı olan Aspose.Words.Drawing.Charts.ChartDataPointCollection sınıfını keşfedin.
type: docs
weight: 980
url: /tr/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Bir koleksiyonu temsil eder[`ChartDataPoint`](../chartdatapoint/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | sayısını döndürür[`ChartDataPoint`](../chartdatapoint/) bu koleksiyonda. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Geri Döndürür[`ChartDataPoint`](../chartdatapoint/) belirtilen dizin için. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Tüm formatları temizler[`ChartDataPoint`](../chartdatapoint/) bu koleksiyonda. |
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(*int, int*) | Biçimi kaynak veri noktasından hedef veri noktasına kopyalar. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(*int*) | Belirtilen dizindeki veri noktasının varsayılan biçime sahip olup olmadığını belirten bir bayrak alır. |

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

* class [ChartDataPoint](../chartdatapoint/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
