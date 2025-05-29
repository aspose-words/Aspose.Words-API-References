---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få åtkomst till ChartSeriesGroup via index med egenskapen Item. Förenkla din datavisualisering och förbättra din diagramupplevelse utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Returnerar en[`ChartSeriesGroup`](../../chartseriesgroup/) vid det angivna indexet.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## Exempel

Visa hur man tar bort sekundäraxeln.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Hitta sekundäraxeln och ta bort den från samlingen.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Se även

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
