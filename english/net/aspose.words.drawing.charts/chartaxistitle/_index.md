---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle class. Provides access to the axis title properties in C#.
type: docs
weight: 650
url: /net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Provides access to the axis title properties.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartAxisTitle
```

## Properties

| Name | Description |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Determines whether other chart elements shall be allowed to overlap the title. The default value is `false`. |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Determines whether the title shall be shown for the axis. The default value is `false`. |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Gets or sets the text of the axis title. If `null` or empty value is specified, auto generated title will be shown. |

## Examples

Shows how to set chart axis title.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Delete default generated series.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Set axis title.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
