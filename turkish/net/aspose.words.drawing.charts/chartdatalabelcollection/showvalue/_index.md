---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: .NET için Aspose.Words
description: ChartDataLabelCollection'daki ShowValue özelliğinin seri değerlerini görüntüleyerek veri görselleştirmenizi nasıl geliştirdiğini keşfedin. Grafiklerinizi bugün optimize edin!
type: docs
weight: 170
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Tüm serinin veri etiketlerinde değerlerin görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` .

```csharp
public bool ShowValue { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, kullanılarak ayrı bir veri etiketi için geçersiz kılınabilir[`ShowValue`](../../chartdatalabel/showvalue/) mülk.

## Örnekler

Pasta grafiğinin veri etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Her sektör için bir kategori adı ve frekans tablosu içeren özel bir grafik serisi ekleyin.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Her sektörün hem yüzdesini hem de frekansını gösterecek veri etiketlerini etkinleştirin ve görünümlerini değiştirin.
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
