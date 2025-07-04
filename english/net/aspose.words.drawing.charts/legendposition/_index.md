---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.Charts.LegendPosition enum to easily customize your chart legend's position for enhanced data visualization.
type: docs
weight: 1220
url: /net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Specifies the possible positions for a chart legend.

```csharp
public enum LegendPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No legend will be shown for the chart. |
| Bottom | `1` | Specifies that the legend shall be drawn at the bottom of the chart. |
| Left | `2` | Specifies that the legend shall be drawn at the left of the chart. |
| Right | `3` | Specifies that the legend shall be drawn at the right of the chart. |
| Top | `4` | Specifies that the legend shall be drawn at the top of the chart. |
| TopRight | `5` | Specifies that the legend shall be drawn at the top right of the chart. |

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
