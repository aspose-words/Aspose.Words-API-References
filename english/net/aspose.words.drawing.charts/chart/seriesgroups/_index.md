---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words for .NET
description: Chart SeriesGroups property. Provides access to a series group collection of this chart in C#.
type: docs
weight: 90
url: /net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Provides access to a series group collection of this chart.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
