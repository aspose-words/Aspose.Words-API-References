---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.ShapeTextOrientation, чтобы легко управлять ориентацией текста в фигурах, улучшая дизайн и читаемость документа.
type: docs
weight: 1680
url: /ru/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Задает ориентацию текста в фигурах.

```csharp
public enum ShapeTextOrientation
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Horizontal | `0` | Текст расположен горизонтально (lr-tb). |
| Downward | `1` | Текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl). |
| Upward | `2` | Текст повернут на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr). |
| VerticalFarEast | `3` | Символы Дальнего Востока отображаются вертикально, остальной текст поворачивается на 90 градусов вправо для отображения сверху вниз (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Символы Дальнего Востока отображаются вертикально, остальной текст поворачивается на 90 градусов вправо, чтобы отображаться сверху вниз по вертикали, затем слева направо по горизонтали (tb-lr-v). |
| WordArtVertical | `5` | Текст вертикальный, одна буква над другой. |
| WordArtVerticalRightToLeft | `6` | Текст вертикальный, одна буква над другой, затем справа налево по горизонтали. |

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
