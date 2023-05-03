---
title: Chart.Legend
linktitle: Legend
second_title: Aspose.Words for .NET API Reference
description: Chart Legend property. Provides access to the chart legend properties in C#.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Provides access to the chart legend properties.

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../chart/)
* assembly [Aspose.Words](../../../)
