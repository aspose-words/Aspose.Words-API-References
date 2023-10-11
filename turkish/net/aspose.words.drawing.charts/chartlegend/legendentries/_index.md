---
title: ChartLegend.LegendEntries
second_title: Aspose.Words for .NET API Referansı
description: ChartLegend mülk. Ana grafiğin tüm serileri ve trend çizgileri için gösterge girişlerinin bir koleksiyonunu döndürür.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

Ana grafiğin tüm serileri ve trend çizgileri için gösterge girişlerinin bir koleksiyonunu döndürür.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

### Örnekler

Grafik serileri için bir açıklama girişiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Ayrıca bakınız

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartlegend/)
* toplantı [Aspose.Words](../../../)


