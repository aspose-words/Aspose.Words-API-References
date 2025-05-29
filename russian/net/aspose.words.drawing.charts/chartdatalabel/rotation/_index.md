---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabel Rotation, чтобы легко настраивать углы меток в ваших диаграммах. Улучшите визуализацию данных с помощью точного управления!
type: docs
weight: 110
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

Получает или задает поворот метки в градусах.

```csharp
public int Rotation { get; set; }
```

## Примечания

Диапазон допустимых значений — от -180 до 180 включительно. Значение по умолчанию — 0.

Если[`Orientation`](../orientation/) значение естьHorizontal форма метки x000d_, если она существует, поворачивается вместе с текстом метки. В противном случае поворачивается только текст метки. x000d_

## Примеры

Показывает, как изменить ориентацию и поворот меток данных.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Показать метки данных.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Определить форму метки данных.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Задаем ориентацию и поворот метки данных для всей серии.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Изменить ориентацию и поворот первой метки данных.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Смотрите также

* class [ChartDataLabel](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
