---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words for .NET
description: ChartSeriesGroup BubbleScale property. Gets or sets the size of the bubbles as a percentage of their default size in C#.
type: docs
weight: 40
url: /net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Gets or sets the size of the bubbles as a percentage of their default size.

```csharp
public int BubbleScale { get; set; }
```

## Remarks

Applies only to series groups of the Bubble and Bubble3D types.

The range of acceptable values is from 0 to 300 inclusive.

## Examples

Show how to set size of the bubbles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a bubble 3D chart.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Set bubble scale to 200%.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### See Also

* class [ChartSeriesGroup](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
