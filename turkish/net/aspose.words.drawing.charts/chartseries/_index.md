---
title: Class ChartSeries
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.ChartSeries sınıf. Grafik serisi özelliklerini temsil eder.
type: docs
weight: 780
url: /tr/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Grafik serisi özelliklerini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartSeries : IChartDataPoint
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Kabarcık grafiğindeki baloncuklara 3 boyutlu efektin uygulanması gerekip gerekmediğini belirtir. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Bu grafik serisi için kabarcık boyutlarının bir koleksiyonunu alır. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Tüm seriye ilişkin veri etiketlerinin ayarlarını belirtir. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Bu serideki tüm veri noktaları için biçimlendirme nesnelerinin bir koleksiyonunu döndürür. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif, özelliğin ayarlanmadığı ve hiçbir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca Pasta grafikleri için geçerlidir. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Serinin dolgu ve çizgi formatlamasına erişim sağlar. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Seri için veri etiketlerinin görüntülenip görüntülenmeyeceğini belirten bir bayrağı alır veya ayarlar. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Değer negatifse ana öğenin renklerini ters çevirip çevirmeyeceğini belirtir. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Bu grafik serisi için bir gösterge girişi alır. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Bir veri işaretçisini belirtir. İşaretleyici istendiğinde otomatik olarak oluşturulur. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Serinin adını alır veya ayarlar; eğer isim açıkça ayarlanmadıysa index. kullanılarak oluşturulur. Varsayılan olarak Seri artı bir tabanlı indeks döndürür. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Bu grafik serisinin türünü alır. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Grafikteki noktaları birleştiren çizginin Catmull-Rom spline'ları kullanılarak yumuşatılıp yumuşatılmayacağını belirlemeye izin verir. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Bu grafik serisi için X değerlerinden oluşan bir koleksiyon alır. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Bu grafik serisi için Y değerlerinin bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(ChartXValue) | Belirtilen X değerini grafik serisine ekler. Seri, Y değerlerini ve kabarcık boyutlarını destekliyorsa, bunlar X değeri için boş olacaktır. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(ChartXValue, ChartYValue) | Belirtilen X ve Y değerlerini grafik serisine ekler. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(ChartXValue, ChartYValue, double) | Belirtilen X değerini, Y değerini ve kabarcık boyutunu grafik serisine ekler. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Tüm veri değerlerini grafik serisinden kaldırır. Tüm bireysel veri noktalarının ve veri etiketlerinin formatı temizlendi. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Veri noktalarının ve veri etiketlerinin formatını koruyarak tüm veri değerlerini grafik serisinden kaldırır. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(int) |  |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(int, ChartXValue) | Belirtilen X değerini belirtilen dizindeki grafik serisine ekler. Seri, Y değerlerini ve kabarcık boyutlarını destekliyorsa, X değeri için boş olacaktır. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(int, ChartXValue, ChartYValue) | Belirtilen X ve Y değerlerini belirtilen dizindeki grafik serisine ekler. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(int, ChartXValue, ChartYValue, double) | Belirtilen X değerini, Y değerini ve kabarcık boyutunu belirtilen dizindeki grafik serisine ekler. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(int) | Belirtilen dizindeki grafik serisinden X değerini, Y değerini ve kabarcık boyutunu (destekleniyorsa) kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır. |

### Örnekler

Çizgi grafikteki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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
    // Bu etiketler grafikteki her veri noktasının yanında görünecek ve değerini gösterecektir.
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

    // Daha temiz görünen bir grafik için veri etiketlerini tek tek kaldırabiliriz.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Ayrıca bir dizi veri etiketinin tamamını aynı anda kaldırabiliriz.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Özel sayı formatına ve ayırıcıya sahip veri etiketlerini bir serideki çeşitli veri noktalarına uygulayın.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
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


