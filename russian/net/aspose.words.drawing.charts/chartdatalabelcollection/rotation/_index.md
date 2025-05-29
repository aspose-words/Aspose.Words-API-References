---
title: ChartDataLabelCollection.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words для .NET
description: Отрегулируйте вращение ChartDataLabelCollection для оптимальной видимости. Настройте углы меток данных, чтобы улучшить читаемость и воздействие вашей диаграммы.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/rotation/
---
## ChartDataLabelCollection.Rotation property

Возвращает или задает поворот меток данных всего ряда в градусах.

```csharp
public int Rotation { get; set; }
```

## Примечания

Диапазон допустимых значений — от -180 до 180 включительно. Значение по умолчанию — 0.

Если[`Orientation`](../orientation/) значение естьHorizontal, формы меток, если они существуют, поворачиваются вместе с текстом метки. В противном случае поворачивается только текст метки.

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

* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
