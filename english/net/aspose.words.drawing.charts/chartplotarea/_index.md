---
title: ChartPlotArea Class
linktitle: ChartPlotArea
articleTitle: ChartPlotArea
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartPlotArea class. Provides access to the plot area properties of a chart.
type: docs
weight: 1090
url: /net/aspose.words.drawing.charts/chartplotarea/
---
## ChartPlotArea class

Provides access to the plot area properties of a chart.

To learn more, visit the [Working with Charts ](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartPlotArea
```

## Properties

| Name | Description |
| --- | --- |
| [Format](../../aspose.words.drawing.charts/chartplotarea/format/) { get; } | Provides access to fill and line formatting of the plot area. |

## Examples

Shows how to set fill and line formatting for the plot area of a chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Delete default generated series and add our own.
ChartSeriesCollection seriesColl = chart.Series;
seriesColl.Clear();
string[] categories = new string[] { "Category 1", "Category 2" };
seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
seriesColl.Add("Series 2", categories, new double[] { 3, 4 });

// Fill the plot area with a gradient and outline it with a thin blue line.
ChartPlotArea plotArea = chart.PlotArea;
plotArea.Format.Fill.OneColorGradient(Color.LightBlue, GradientStyle.DiagonalUp, GradientVariant.Variant2, 1);
plotArea.Format.Stroke.ForeColor = Color.Blue;
plotArea.Format.Stroke.Weight = 0.25;

doc.Save(ArtifactsDir + "Charts.PlotAreaFormat.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
