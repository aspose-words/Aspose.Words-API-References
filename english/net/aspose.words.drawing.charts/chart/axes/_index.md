---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words for .NET
description: Chart Axes property. Gets a collection of all axes of this chart in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Gets a collection of all axes of this chart.

```csharp
public ChartAxisCollection Axes { get; }
```

## Examples

Shows how to work with axes collection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Hide the major grid lines on the primary and secondary Y axes.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### See Also

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
