---
title: Class ChartAxisCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartAxisCollection сорт. Представляет коллекцию осей диаграммы.
type: docs
weight: 640
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

### Примеры

Показывает, как работать с коллекцией осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Скрываем основные линии сетки на первичной и вторичной осях Y.
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


