---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: ChartLegend Position property. Specifies the position of the legend on a chart in C#.
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

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

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
