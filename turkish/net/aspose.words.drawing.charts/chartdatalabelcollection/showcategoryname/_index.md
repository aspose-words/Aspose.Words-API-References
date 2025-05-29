---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: .NET için Aspose.Words
description: ChartDataLabelCollection'daki ShowCategoryName özelliğini keşfedin. Serileriniz için veri etiketi görünürlüğünü kontrol edin ve grafiğinizin netliğini artırın!
type: docs
weight: 110
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

Tüm serinin veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Varsayılan değer`YANLIŞ` .

```csharp
public bool ShowCategoryName { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, kullanılarak ayrı bir veri etiketi için geçersiz kılınabilir[`ShowCategoryName`](../../chartdatalabel/showcategoryname/) mülk.

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

### Ayrıca bakınız

* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
