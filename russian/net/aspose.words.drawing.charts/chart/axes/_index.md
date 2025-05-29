---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Chart Axes для доступа ко всем осям диаграммы без усилий. Улучшите визуализацию данных с помощью комплексного управления осями.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Получает коллекцию всех осей этой диаграммы.

```csharp
public ChartAxisCollection Axes { get; }
```

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

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
