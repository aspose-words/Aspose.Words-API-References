---
title: Class ChartDataLabel
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.ChartDataLabel sınıf. Bir grafik noktasındaki veya trend çizgisindeki veri etiketini temsil eder.
type: docs
weight: 670
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Bir grafik noktasındaki veya trend çizgisindeki veri etiketini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartDataLabel
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Bu veri etiketinin yazı tipi formatına erişim sağlar. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Veri etiketinin dolgu ve satır formatlamasına erişim sağlar. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | İçeren öğenin dizinini belirtir. Bu dizin, bu öğenin ebeveynin alt koleksiyonundan hangisine uygulanacağını belirleyecektir. Varsayılan değer 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Bu etiketin gizli olup olmadığını belirten bir bayrak alır/ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | İadeler`doğru` bu veri etiketinde görüntülenecek bir şey varsa. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Ana öğenin sayı biçimini döndürür. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Grafikteki veri etiketleri için kullanılan dize ayırıcıyı alır veya ayarlar. Yalnızca kategori adını ve yüzdesini gösteren pasta grafikleri dışında varsayılan değer virgüldür; bunun yerine satır sonu kullanılacaktır. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Bir grafikteki veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Yalnızca Kabarcık grafikleri için geçerlidir. Varsayılan değer:`YANLIŞ` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Bir grafikteki veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Veri etiketleri aralığındaki değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer:`YANLIŞ` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Veri etiketi öncü çizgilerinin gösterilmesi gerekip gerekmediğini belirlemeye olanak tanır. Varsayılan değer:`YANLIŞ` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Bir grafikteki veri etiketleri için açıklama anahtarının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Bir grafikteki veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirlemeye olanak sağlar. Varsayılan değer:`YANLIŞ` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Grafikteki veri etiketleri için seri adı görüntüleme davranışını belirtmek üzere bir Boole değeri döndürür veya ayarlar. `doğru` seri adını göstermek için;`YANLIŞ` saklanmak. Varsayılan olarak`YANLIŞ` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Veri etiketlerinde değerlerin görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer:`YANLIŞ` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Bu veri etiketinin biçimini temizler. Özellikler, üst data etiket koleksiyonunda tanımlanan varsayılan değerlere ayarlanır. |

### Notlar

Bir seride,`ChartDataLabel` nesnenin bir üyesidir[`ChartDataLabelCollection`](../chartdatalabelcollection/) . [`ChartDataLabelCollection`](../chartdatalabelcollection/) içerir`ChartDataLabel` Her nokta için nesne.

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


