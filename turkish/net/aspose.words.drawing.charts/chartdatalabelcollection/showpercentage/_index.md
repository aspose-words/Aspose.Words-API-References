---
title: ChartDataLabelCollection.ShowPercentage
linktitle: ShowPercentage
articleTitle: ShowPercentage
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection ShowPercentage mülk. Tüm serinin veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değerYANLIŞ . Yalnızca Pasta grafikleri için geçerlidir C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

Tüm serinin veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. Varsayılan değer:`YANLIŞ` . Yalnızca Pasta grafikleri için geçerlidir.

```csharp
public bool ShowPercentage { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, the kullanılarak tek bir veri etiketi için geçersiz kılınabilir[`ShowPercentage`](../../chartdatalabel/showpercentage/) özellik.

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
