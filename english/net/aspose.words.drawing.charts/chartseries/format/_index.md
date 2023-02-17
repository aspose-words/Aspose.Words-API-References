---
title: ChartSeries.Format
second_title: Aspose.Words for .NET API Reference
description: ChartSeries property. Provides access to fill and line formatting of the series in C#.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Provides access to fill and line formatting of the series.

```csharp
public ChartFormat Format { get; }
```

## Examples

Sows how to set series color.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Delete default generated series.
seriesColl.Clear();

// Create category names array.
string[] categories = new[] { "Category 1", "Category 2" };

// Adding new series. Value and category arrays must be the same size.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Set series color.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### See Also

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartseries/)
* assembly [Aspose.Words](../../../)
