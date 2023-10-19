---
title: ChartDataLabelCollection.ShowSeriesName
linktitle: ShowSeriesName
articleTitle: ShowSeriesName
second_title: Aspose.Words for .NET
description: ChartDataLabelCollection ShowSeriesName mülk. Tüm serinin veri etiketleri için seri adı görüntüleme davranışını belirtmek üzere bir Boole değeri döndürür veya ayarlar. doğru seri adını göstermek içinYANLIŞ saklanmak. Varsayılan olarakYANLIŞ  C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

Tüm serinin veri etiketleri için seri adı görüntüleme davranışını belirtmek üzere bir Boole değeri döndürür veya ayarlar. `doğru` seri adını göstermek için;`YANLIŞ` saklanmak. Varsayılan olarak`YANLIŞ` .

```csharp
public bool ShowSeriesName { get; set; }
```

## Notlar

Bu özellik için tanımlanan değer, the kullanılarak tek bir veri etiketi için geçersiz kılınabilir[`ShowSeriesName`](../../chartdatalabel/showseriesname/) özellik.

## Örnekler

Kabarcık grafiğinin veri etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X/Y koordinatlarını ve her bir balonun çapını içeren özel bir seri ekleyin.
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
