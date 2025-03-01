---
title: ChartTitle.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: Explore the ChartTitle Format property for enhanced fill and line styling, giving your charts a professional and polished look.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/charttitle/format/
---
## ChartTitle.Format property

Provides access to fill and line formatting of the chart title.

```csharp
public ChartFormat Format { get; }
```

## Examples

Shows how to use chart formating.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Delete series generated by default.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Format chart background.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Hide axis tick labels.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Format chart title.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Format axis title.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Format legend.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### See Also

* class [ChartFormat](../../chartformat/)
* class [ChartTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
