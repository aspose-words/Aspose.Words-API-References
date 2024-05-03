---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words for .NET
description: ChartSeriesGroup Overlap property. Gets or sets the percentage of how much the series bars or columns overlap in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Gets or sets the percentage of how much the series bars or columns overlap.

```csharp
public int Overlap { get; set; }
```

## Remarks

Applies to series groups of all bar and column types.

The range of acceptable values is from -100 to 100 inclusive. A value of 0 indicates that there is no space between bars/columns. If the value is -100, the distance between bars/columns is equal to their width. A value of 100 means that the bars/columns overlap completely.

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
