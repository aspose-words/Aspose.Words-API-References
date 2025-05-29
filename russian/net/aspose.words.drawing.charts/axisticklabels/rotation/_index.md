---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words для .NET
description: Отрегулируйте вращение AxisTickLabels для оптимальной читаемости. Настройте углы меток делений в градусах, чтобы улучшить четкость и визуальную привлекательность диаграммы.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Возвращает или задает поворот меток делений в градусах.

```csharp
public int Rotation { get; set; }
```

## Примечания

Диапазон допустимых значений от -180 до 180 включительно. Значение по умолчанию 0.

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

* class [AxisTickLabels](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
