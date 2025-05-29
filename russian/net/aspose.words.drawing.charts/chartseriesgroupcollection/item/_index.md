---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Доступ к ChartSeriesGroup по индексу с помощью свойства Item. Упростите визуализацию данных и улучшите свой опыт построения диаграмм без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Возвращает[`ChartSeriesGroup`](../../chartseriesgroup/) по указанному индексу.

```csharp
public ChartSeriesGroup this[int index] { get; }
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

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
