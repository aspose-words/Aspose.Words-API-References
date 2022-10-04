---
title: ChartDataLabel
second_title: Aspose.Words for .NET API Referansı
description: Bir grafik noktası veya eğilim çizgisi üzerindeki veri etiketini temsil eder.
type: docs
weight: 630
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Bir grafik noktası veya eğilim çizgisi üzerindeki veri etiketini temsil eder.

```csharp
public class ChartDataLabel
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | İçeren öğenin dizinini belirtir. Bu dizin, bu öğenin hangi ebeveynin çocuk koleksiyonuna uygulanacağını belirler. Varsayılan değer 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Bu etiketin gizli olup olmadığını gösteren bir bayrak alır/ayarlar. Varsayılan değer **yanlış** . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Bu veri etiketinin görüntülenecek bir şeyi varsa doğru döndürür. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Üst öğenin sayı biçimini döndürür. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Bir grafikteki veri etiketleri için kullanılan dize ayırıcısını alır veya ayarlar. Bunun yerine bir satır sonu kullanılacaksa, yalnızca kategori adını ve yüzdeyi gösteren pasta grafikler hariç, varsayılan değer bir virgüldür. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Bir grafikteki veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Yalnızca Kabarcık çizelgeleri için geçerlidir. Varsayılan değer yanlıştır. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Bir grafikteki veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer yanlıştır. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Veri etiketlerindeki değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer yanlıştır. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Veri etiketi öncü çizgilerinin gösterilmesi gerekip gerekmediğini belirlemeye izin verir. Varsayılan değer yanlıştır. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Bir grafikteki veri etiketleri için gösterge anahtarının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer yanlıştır. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Bir grafikteki veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer yanlıştır. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Bir grafikteki veri etiketleri için seri adı görüntüleme davranışını belirtmek için bir Boole döndürür veya ayarlar. Seri adını göstermek için doğru. Gizlemek için yanlış. Varsayılan olarak false. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer yanlıştır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Bu veri etiketinin biçimini temizler. Özellikler, ana data etiket koleksiyonunda tanımlanan varsayılan değerlere ayarlanır. |

### Notlar

Bir dizide,[`ChartDataLabel`](./chartdatalabel/) nesne üyedir[`ChartDataLabelCollection`](../chartdatalabelcollection/) . [`ChartDataLabelCollection`](../chartdatalabelcollection/) içerir[`ChartDataLabel`](./chartdatalabel/) Her nokta için nesne.

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
