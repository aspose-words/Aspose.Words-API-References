---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words для .NET
description: Легко удалите группу серий с помощью метода ChartSeriesGroupCollection RemoveAt. Упростите управление диаграммами, удалив ненужные данные.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Удаляет группу серий по указанному индексу. Все дочерние серии будут удалены из диаграммы.

```csharp
public void RemoveAt(int index)
```

## Примеры

Покажите, как удалить вторичную ось.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Найти вторичную ось и удалить из коллекции.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Смотрите также

* class [ChartSeriesGroupCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
