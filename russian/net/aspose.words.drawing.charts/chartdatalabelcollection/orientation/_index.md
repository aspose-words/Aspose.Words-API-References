---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabelCollection Orientation, которое позволяет легко настраивать ориентацию текста для подписей данных, повышая ясность и эффективность диаграммы.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

Возвращает или задает ориентацию текста меток данных всей серии.

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
* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
