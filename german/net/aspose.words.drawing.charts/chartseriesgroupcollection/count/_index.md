---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Count-Eigenschaft von ChartSeriesGroupCollection, die die Gesamtzahl der Seriengruppen zur verbesserten Datenvisualisierung anzeigt.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

Gibt die Anzahl der Seriengruppen in dieser Sammlung zurück.

```csharp
public int Count { get; }
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

* class [ChartSeriesGroupCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
