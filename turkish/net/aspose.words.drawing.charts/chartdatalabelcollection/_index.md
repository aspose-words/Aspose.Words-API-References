---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: .NET için Aspose.Words
description: Grafik veri etiketlerini verimli bir şekilde yönetmek için Aspose.Words.ChartDataLabelCollection sınıfını keşfedin. Belgenizin görsel çekiciliğini bugün artırın!
type: docs
weight: 940
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Bir koleksiyonu temsil eder[`ChartDataLabel`](../chartdatalabel/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | sayısını döndürür[`ChartDataLabel`](../chartdatalabel/) bu koleksiyonda. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Tüm serinin veri etiketlerinin yazı tipi biçimlendirmesine erişim sağlar. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Veri etiketlerinin dolgu ve satır biçimlendirmesine erişim sağlar. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Geri Döndürür[`ChartDataLabel`](../chartdatalabel/) belirtilen dizin için. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Bir alır[`ChartNumberFormat`](../chartnumberformat/) serisinin veri etiketleri için sayı biçimini ayarlamaya izin veren örnek. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabelcollection/orientation/) { get; set; } | Tüm serinin veri etiketlerinin metin yönünü alır veya ayarlar. |
| [Position](../../aspose.words.drawing.charts/chartdatalabelcollection/position/) { get; set; } | Veri etiketlerinin konumunu alır veya ayarlar. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabelcollection/rotation/) { get; set; } | Tüm serinin veri etiketlerinin derece cinsinden dönüşünü alır veya ayarlar. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Tüm serinin veri etiketleri için kullanılan dize ayırıcısını alır veya ayarlar. Varsayılan değer virgüldür, ancak yalnızca kategori adını ve yüzdeyi gösteren pasta grafikleri için bunun yerine satır sonu kullanılır. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Tüm serinin veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Yalnızca Kabarcık grafikleri için geçerlidir. Varsayılan değer`YANLIŞ` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Tüm serinin veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Veri etiketi aralığındaki değerlerin tüm serinin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Tüm serinin veri etiketleri için veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Tüm serinin veri etiketleri için efsane anahtarının görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Tüm serinin veri etiketleri için yüzdelik değerin görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . Yalnızca Pasta grafikleri için geçerlidir. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Tüm serinin veri etiketleri için seri adı görüntüleme davranışını belirtmek üzere bir Boole değeri döndürür veya ayarlar. `doğru` dizi adını göstermek için;`YANLIŞ` gizlemek için. Varsayılan olarak`YANLIŞ` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Tüm serinin veri etiketlerinde değerlerin görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Tüm formatları temizler[`ChartDataLabel`](../chartdatalabel/) bu koleksiyonda. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |

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

* class [ChartDataLabel](../chartdatalabel/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
