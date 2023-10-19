---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: ChartSeries Format mülk. Serinin dolgu ve çizgi formatlamasına erişim sağlar C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Serinin dolgu ve çizgi formatlamasına erişim sağlar.

```csharp
public ChartFormat Format { get; }
```

## Örnekler

Seri renginin nasıl ayarlanacağını anlatır.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Varsayılan olarak oluşturulan seriyi silin.
seriesColl.Clear();

// Kategori adları dizisini oluşturun.
string[] categories = new[] { "Category 1", "Category 2" };

//Yeni seriler ekleniyor. Değer ve kategori dizileri aynı boyutta olmalıdır.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Seri rengini ayarlayın.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Ayrıca bakınız

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
