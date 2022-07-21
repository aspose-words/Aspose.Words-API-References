---
title: ChartDataLabelCollection
second_title: Aspose.Words for .NET API Referansı
description: Bir koleksiyonu temsil ederChartDataLabel./chartdatalabel .
type: docs
weight: 640
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Bir koleksiyonu temsil eder[`ChartDataLabel`](../chartdatalabel) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count) { get; } | Sayısını döndürür[`ChartDataLabel`](../chartdatalabel) bu koleksiyonda. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item) { get; } | İade[`ChartDataLabel`](../chartdatalabel) belirtilen dizin için. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat) { get; } | Bir[`ChartNumberFormat`](../chartnumberformat) tüm serinin veri etiketleri için sayı biçimini ayarlamaya izin veren örnek. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator) { get; set; } | Tüm serinin veri etiketleri için kullanılan dize ayırıcısını alır veya ayarlar. Bunun yerine bir satır sonu kullanılacaksa, yalnızca kategori adını ve yüzdeyi gösteren pasta grafikler hariç, varsayılan değer bir virgüldür. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize) { get; set; } | Tüm serinin veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Yalnızca Kabarcık grafikleri için geçerlidir. Varsayılan değer **yanlış** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname) { get; set; } | Tüm serinin veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer **yanlış** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange) { get; set; } | Veri etiketleri aralığındaki değerlerin tüm serinin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer **yanlış** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines) { get; set; } | Tüm serinin veri etiketleri için veri etiketi öncü çizgilerinin gösterilmesi gerekip gerekmediğini belirlemeye izin verir. Varsayılan değer **yanlış** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey) { get; set; } | Tüm serinin veri etiketleri için gösterge anahtarının görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer **yanlış** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage) { get; set; } | Tüm serinin veri etiketleri için yüzde değerinin gösterilip gösterilmeyeceğini belirlemeye izin verir. Varsayılan değer **yanlış** . Yalnızca Pasta grafikler için geçerlidir. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname) { get; set; } | Tüm serinin veri etiketleri için seri adı görüntüleme davranışını belirtmek için bir Boole döndürür veya ayarlar.  **Doğru**dizi adını göstermek için **Yanlış** gizlemek için. Varsayılan olarak **yanlış** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue) { get; set; } | Tüm serinin veri etiketlerinde değerlerin gösterilip gösterilmeyeceğini belirlemeye izin verir. Varsayılan değer **yanlış** . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat)() | Tümünün biçimini temizler[`ChartDataLabel`](../chartdatalabel) bu koleksiyonda. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator)() | Bir numaralandırıcı nesnesi döndürür. |

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

* class [ChartDataLabel](../chartdatalabel)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
