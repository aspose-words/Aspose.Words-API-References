---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mit der Item-Eigenschaft über den Index auf ChartSeriesGroup zu. Vereinfachen Sie Ihre Datenvisualisierung und verbessern Sie mühelos Ihre Diagrammerstellung!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Gibt einen[`ChartSeriesGroup`](../../chartseriesgroup/) am angegebenen Index.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## Beispiele

Zeigen Sie, wie die sekundäre Achse entfernt wird.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Sekundärachse suchen und aus der Sammlung entfernen.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Siehe auch

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
