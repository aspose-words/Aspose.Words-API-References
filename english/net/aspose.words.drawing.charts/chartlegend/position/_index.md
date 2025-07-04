---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: Discover the ChartLegend Position property to easily customize your chart's legend placement for enhanced clarity and visual appeal.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Specifies the position of the legend on a chart.

```csharp
public LegendPosition Position { get; set; }
```

## Remarks

The default value is Right for pre-Word 2016 charts and Top for Word 2016 charts.

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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
