---
title: ChartDataLabelCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection Item mülk. İadelerChartDataLabel belirtilen dizin için C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/item/
---
## ChartDataLabelCollection indexer

İadeler[`ChartDataLabel`](../../chartdatalabel/) belirtilen dizin için.

```csharp
public ChartDataLabel this[int index] { get; }
```

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

* class [ChartDataLabel](../../chartdatalabel/)
* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
