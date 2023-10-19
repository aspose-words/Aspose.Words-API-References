---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection sınıf. Aşağıdakilerin bir koleksiyonunu temsil ederChartDataLabel  C#'da.
type: docs
weight: 680
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Aşağıdakilerin bir koleksiyonunu temsil eder:[`ChartDataLabel`](../chartdatalabel/) .

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Sayıyı döndürür[`ChartDataLabel`](../chartdatalabel/) bu koleksiyonda. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Tüm serinin veri etiketlerinin yazı tipi formatlamasına erişim sağlar. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Veri etiketlerinin dolgu ve satır formatına erişim sağlar. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | İadeler[`ChartDataLabel`](../chartdatalabel/) belirtilen dizin için. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Bir alır[`ChartNumberFormat`](../chartnumberformat/) the serisinin tamamının veri etiketleri için sayı formatını ayarlamaya izin veren örnek. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Tüm serinin veri etiketleri için kullanılan dize ayırıcıyı alır veya ayarlar. Yalnızca kategori adını ve yüzdesini gösteren pasta grafikleri dışında varsayılan değer virgüldür; bunun yerine satır sonu kullanılacaktır. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Tüm serinin veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Yalnızca Kabarcık grafikleri için geçerlidir. Varsayılan değer:`YANLIŞ` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Tüm serinin veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Veri etiketleri aralığındaki değerlerin tüm serinin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Tüm serinin veri etiketleri için veri etiketi lider çizgilerinin gösterilmesinin gerekip gerekmediğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Tüm serinin veri etiketleri için açıklama anahtarının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Tüm serinin veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer:`YANLIŞ` . Yalnızca Pasta grafikleri için geçerlidir. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Tüm serinin veri etiketleri için seri adı görüntüleme davranışını belirtmek üzere bir Boole değeri döndürür veya ayarlar. `doğru` seri adını göstermek için;`YANLIŞ` saklanmak. Varsayılan olarak`YANLIŞ` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Tüm serinin veri etiketlerinde değerlerin görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Tümünün biçimini temizler[`ChartDataLabel`](../chartdatalabel/) bu koleksiyonda. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |

## Örnekler

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

* class [ChartDataLabel](../chartdatalabel/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
