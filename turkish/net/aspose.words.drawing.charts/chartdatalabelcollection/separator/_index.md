---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: .NET için Aspose.Words
description: ChartDataLabelCollection'ın Ayırıcı özelliğini keşfedin. Grafiklerinizde virgüllerden satır sonlarına kadar gelişmiş netlik için veri etiketi ayırıcılarını özelleştirin.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Tüm serinin veri etiketleri için kullanılan dize ayırıcısını alır veya ayarlar. Varsayılan değer virgüldür, ancak yalnızca kategori adını ve yüzdeyi gösteren pasta grafikleri için bunun yerine satır sonu kullanılır.

```csharp
public string Separator { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, kullanılarak ayrı bir veri etiketi için geçersiz kılınabilir[`Separator`](../../chartdatalabel/separator/) mülk.

## Örnekler

Bir kabarcık grafiğinin veri etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

 // Her bir baloncuğun X/Y koordinatları ve çapı ile özel bir seri ekleyin.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Veri etiketlerini etkinleştirin ve ardından görünümlerini değiştirin.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

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
