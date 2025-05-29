---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words для .NET
description: Настройте ориентацию AxisTickLabels для оптимальной читаемости. Легко настройте направление текста метки галочки, чтобы улучшить визуализацию данных!
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Возвращает или задает ориентацию текста метки деления.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Примечания

Значение по умолчанию:Horizontal.

Обратите внимание, что некоторые[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) значения не влияют на ориентацию метки отметки text на осях значений.

## Примеры

Показывает, как изменить ориентацию и поворот меток делений осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить столбчатую диаграмму.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Задаем ориентацию и поворот метки деления оси.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Смотрите также

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
