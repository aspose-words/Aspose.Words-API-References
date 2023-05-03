---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartAxisCollection class. Represents a collection of chart axes in C#.
type: docs
weight: 630
url: /net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Represents a collection of chart axes.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Gets the number of axes in this collection. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Gets the axis at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Returns an enumerator object. |

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

* class [ChartAxis](../chartaxis/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
