---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words for .NET
description: ChartSeriesGroup GapWidth property. Gets or sets the percentage of gap width between chart elements in C#.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Gets or sets the percentage of gap width between chart elements.

```csharp
public int GapWidth { get; set; }
```

## Remarks

Applies only to series groups of the bar, column, pie-of-bar, pie-of-pie, histogram, box&amp;whisker, waterfall and funnel types.

The range of acceptable values is from 0 to 500 inclusive. For bar/column-based series groups, the property represents the space between bar clusters as a percentage of their width. For pie-of-pie and bar-of-pie charts, this is the space between the primary and secondary sections of the chart.

## Examples

Show how to configure gap width and overlap.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Set column gap width and overlap.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### See Also

* class [ChartSeriesGroup](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
