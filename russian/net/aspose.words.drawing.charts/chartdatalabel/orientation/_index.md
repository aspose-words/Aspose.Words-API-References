---
title: ChartDataLabel.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabel Orientation, позволяющее легко настраивать ориентацию текста меток для улучшения визуализации данных и ясности ваших диаграмм.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/orientation/
---
## ChartDataLabel.Orientation property

Получает или задает ориентацию текста метки.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Примечания

Значение по умолчанию:Horizontal .

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabel](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
