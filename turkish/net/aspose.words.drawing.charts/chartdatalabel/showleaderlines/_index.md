---
title: ChartDataLabel.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: .NET için Aspose.Words
description: ChartDataLabel'daki ShowLeaderLines özelliğiyle grafiklerinizi geliştirin. Daha net veri görselleştirmesi için veri etiketi lider çizgilerini kolayca görüntüleyin.
type: docs
weight: 160
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/showleaderlines/
---
## ChartDataLabel.ShowLeaderLines property

Veri etiketi lider çizgilerinin gösterilmesi gerekip gerekmediğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## Notlar

Yalnızca Pasta grafikleri için geçerlidir. Lider çizgiler, bir veri etiketi ile karşılık gelen veri noktası arasında görsel bir bağlantı oluşturur.

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

* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
