---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection ShowValue mülk. Tüm serinin veri etiketlerinde değerlerin görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Tüm serinin veri etiketlerinde değerlerin görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ShowValue { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, the kullanılarak tek bir veri etiketi için geçersiz kılınabilir[`ShowValue`](../../chartdatalabel/showvalue/) özellik.

## Örnekler

Pasta grafiğinin veri etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Sektörlerin her biri için kategori adını ve bunların frekans tablosunu içeren özel bir grafik serisi ekleyin.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Her sektörün hem yüzdesini hem de sıklığını görüntüleyecek veri etiketlerini etkinleştirin ve görünümlerini değiştirin.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Ayrıca bakınız

* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
