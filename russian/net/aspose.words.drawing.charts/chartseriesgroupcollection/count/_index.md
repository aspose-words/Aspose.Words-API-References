---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Count объекта ChartSeriesGroupCollection, которое отображает общее количество групп рядов для улучшенной визуализации данных.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

Возвращает количество групп серий в этой коллекции.

```csharp
public int Count { get; }
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
