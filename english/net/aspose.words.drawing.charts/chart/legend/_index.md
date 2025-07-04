---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words for .NET
description: Discover the Chart Legend property to customize your charts effortlessly. Enhance data visualization with tailored legend options for better insights!
type: docs
weight: 70
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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
