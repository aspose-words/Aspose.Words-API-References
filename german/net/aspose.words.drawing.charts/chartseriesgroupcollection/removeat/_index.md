---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos eine Seriengruppe mit der Methode „RemoveAt“ der ChartSeriesGroupCollection. Vereinfachen Sie Ihre Diagrammverwaltung, indem Sie unerwünschte Daten entfernen.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Entfernt eine Seriengruppe am angegebenen Index. Alle untergeordneten Serien werden aus dem Diagramm entfernt.

```csharp
public void RemoveAt(int index)
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
