---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.ChartLegend class to enhance your charts with customizable legend properties for better data visualization.
type: docs
weight: 1000
url: /net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Represents chart legend properties.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/net/working-with-charts/) documentation article.

```csharp
public class ChartLegend
```

## Properties

| Name | Description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Provides access to the default font formatting of legend entries. To override the font formatting for a specific legend entry, use the[`Font`](../chartlegendentry/font/) property. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Provides access to fill and line formatting of the legend. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Returns a collection of legend entries for all series and trendlines of the parent chart. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Determines whether other chart elements shall be allowed to overlap legend. Default value is `false`. |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Specifies the position of the legend on a chart. |

## Examples

Shows how to edit the appearance of a chart's legend.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.That(chart.Series.Count, Is.EqualTo(3));
Assert.That(chart.Series[0].Name, Is.EqualTo("Series 1"));
Assert.That(chart.Series[1].Name, Is.EqualTo("Series 2"));
Assert.That(chart.Series[2].Name, Is.EqualTo("Series 3"));

// Move the chart's legend to the top right corner.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
