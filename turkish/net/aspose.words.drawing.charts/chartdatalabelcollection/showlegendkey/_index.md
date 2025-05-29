---
title: ChartDataLabelCollection.ShowLegendKey
linktitle: ShowLegendKey
articleTitle: ShowLegendKey
second_title: .NET için Aspose.Words
description: ChartDataLabelCollection'daki ShowLegendKey özelliğiyle grafiğinizin görünümünü kontrol edin. Gelişmiş veri netliği için efsane tuşlarını kolayca değiştirin.
type: docs
weight: 140
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/
---
## ChartDataLabelCollection.ShowLegendKey property

Tüm serinin veri etiketleri için efsane anahtarının görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` .

```csharp
public bool ShowLegendKey { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, kullanılarak ayrı bir veri etiketi için geçersiz kılınabilir[`ShowLegendKey`](../../chartdatalabel/showlegendkey/) mülk.

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
