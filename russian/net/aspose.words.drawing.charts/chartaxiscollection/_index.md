---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ChartAxisCollection — ваше идеальное решение для эффективного управления осями диаграммы и улучшения визуализации данных вашего документа.
type: docs
weight: 900
url: /ru/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Представляет коллекцию осей диаграммы.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Получает количество осей в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Получает ось по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Возвращает объект перечислителя. |

## Примеры

Показывает, как работать с коллекцией осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Скрыть основные линии сетки на первичной и вторичной осях Y.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Смотрите также

* class [ChartAxis](../chartaxis/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
