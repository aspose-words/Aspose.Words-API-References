---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: ChartSeriesGroupCollection RemoveAt method. Removes a series group at the specified index. All child series will be removed from the chart in C#.
type: docs
weight: 50
url: /net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Removes a series group at the specified index. All child series will be removed from the chart.

```csharp
public void RemoveAt(int index)
```

## Examples

Show how to remove secondary axis.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Find secondary axis and remove from the collection.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### See Also

* class [ChartSeriesGroupCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
