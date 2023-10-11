---
title: Chart.Axes
second_title: Справочник по API Aspose.Words для .NET
description: Chart свойство. Получает коллекцию всех осей этой диаграммы.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Получает коллекцию всех осей этой диаграммы.

```csharp
public ChartAxisCollection Axes { get; }
```

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

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chart/)
* сборка [Aspose.Words](../../../)


