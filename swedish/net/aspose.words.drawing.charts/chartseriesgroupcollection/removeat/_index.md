---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words för .NET
description: Ta enkelt bort en seriegrupp med metoden ChartSeriesGroupCollection RemoveAt. Förenkla din diagramhantering genom att eliminera oönskad data.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Tar bort en seriegrupp vid det angivna indexet. Alla underserier tas bort från diagrammet.

```csharp
public void RemoveAt(int index)
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

* class [ChartSeriesGroupCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
