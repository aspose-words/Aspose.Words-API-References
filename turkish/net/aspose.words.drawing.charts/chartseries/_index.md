---
title: Class ChartSeries
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.ChartSeries sınıf. Grafik serisi özelliklerini temsil eder.
type: docs
weight: 730
url: /tr/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Grafik serisi özelliklerini temsil eder.

```csharp
public class ChartSeries : IChartDataPoint
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } |  |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Tüm seri için veri etiketleri için ayarları belirtir. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Bu serideki tüm veri noktaları için bir biçimlendirme nesneleri koleksiyonu döndürür. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Serinin dolgu ve satır biçimlendirmesine erişim sağlar. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Seri için veri etiketlerinin görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } |  |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Bu grafik serisi için bir gösterge girişi alır. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } |  |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Dizinin adını alır veya ayarlar, ad açıkça ayarlanmadıysa dizin kullanılarak oluşturulur. Varsayılan olarak Seri artı bir tabanlı dizin döndürür. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Grafikteki noktaları birleştiren çizginin Catmull-Rom spline'ları kullanılarak düzleştirilip düzleştirilmeyeceğini belirlemeye izin verir. |

### Örnekler

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```csharp
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

    // Bir dizideki her veri etiketi için ayırıcı dizeyi değiştirin.
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

    // Veri etiketlerinin tamamını bir kerede de kaldırabiliriz.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Bir dizideki birkaç veri noktasına özel sayı formatı ve ayırıcı ile veri etiketleri uygulayın.
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


