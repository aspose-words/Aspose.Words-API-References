---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: .NET için Aspose.Words
description: Dinamik belge oluşturma ve görselleştirme için grafik serisi özelliklerini geliştirmenin anahtarı olan Aspose.Words.Drawing.Charts.ChartSeries sınıfını keşfedin.
type: docs
weight: 1070
url: /tr/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Grafik serisi özelliklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartSeries : IChartDataPoint
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Kabarcık grafiğindeki kabarcıklara 3 boyutlu efekt uygulanıp uygulanmayacağını belirtir. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Bu grafik serisi için bir dizi kabarcık boyutu alır. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Tüm seri için veri etiketlerinin ayarlarını belirtir. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Bu serideki tüm veri noktaları için biçimlendirme nesnelerinin bir koleksiyonunu döndürür. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif özelliğin ayarlanmadığı ve herhangi bir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca pasta grafikleri için geçerlidir. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Serinin dolgu ve satır biçimlendirmesine erişim sağlar. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Seri için veri etiketlerinin görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Değer negatifse üst öğenin renklerini tersine çevirip çevirmeyeceğini belirtir. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Bu grafik serisi için bir gösterge girişi alır. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Bir veri işaretçisi belirtir. İşaretleyici, talep edildiğinde otomatik olarak oluşturulur. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Serinin adını alır veya ayarlar; ad açıkça ayarlanmamışsa index. kullanılarak oluşturulur. Varsayılan olarak Seri artı bir tabanlı index. değerini döndürür. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Bu grafik serisinin türünü alır. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Grafikteki noktaları birleştiren çizginin Catmull-Rom spline'ları kullanılarak düzeltilip düzeltilmeyeceğini belirtmeye olanak tanır. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Bu grafik serisi için X değerlerinin bir koleksiyonunu alır. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Bu grafik serisi için Y değerlerinin bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Belirtilen X değerini grafik serisine ekler. Seri Y değerlerini ve baloncuk boyutlarını destekliyorsa, X değeri için boş olacaklardır. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Belirtilen X ve Y değerlerini grafik serisine ekler. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Grafik serisine belirtilen X değerini, Y değerini ve kabarcık boyutunu ekler. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Grafik serisinden tüm veri değerlerini kaldırır. Tüm bireysel veri noktalarının ve veri etiketlerinin biçimi temizlenir. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Veri noktalarının ve veri etiketlerinin biçimini koruyarak grafik serisinden tüm veri değerlerini kaldırır. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | Belirtilen endekse sahip veri noktasından varsayılan veri noktası biçimini kopyalar. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Belirtilen X değerini belirtilen dizindeki grafik serisine ekler. Seri Y değerlerini ve kabarcık boyutlarını destekliyorsa, X değeri için boş olacaklardır. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Belirtilen X ve Y değerlerini belirtilen dizindeki grafik serisine ekler. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Belirtilen X değerini, Y değerini ve kabarcık boyutunu belirtilen dizindeki grafik serisine ekler. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Destekleniyorsa, belirtilen dizindeki grafik serisinden X değerini, Y değerini ve kabarcık boyutunu kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır. |

## Örnekler

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Grafikteki her seriye veri etiketleri uygulayın.
    // Bu etiketler, grafikteki her veri noktasının yanında görünecek ve değerini gösterecektir.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Bir serideki her veri etiketi için ayırıcı dizeyi değiştirin.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // Daha temiz görünümlü bir grafik için veri etiketlerini tek tek kaldırabiliriz.
    dataLabel.ClearFormat();

    // Ayrıca bir dizi verinin tüm etiketlerini bir kerede kaldırabiliriz.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Bir serideki birden fazla veri noktasına özel sayı biçimi ve ayırıcı ile veri etiketleri uygulayın.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### Ayrıca bakınız

* interface [IChartDataPoint](../ichartdatapoint/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
