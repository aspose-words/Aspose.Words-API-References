---
title: Enum DashStyle
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.DashStyle перечисление. Стиль пунктирной линии.
type: docs
weight: 930
url: /ru/net/aspose.words.drawing/dashstyle/
---
## DashStyle enumeration

Стиль пунктирной линии.

```csharp
public enum DashStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Solid | `0` | Сплошное (непрерывное) перо. |
| ShortDash | `1` | Стиль системного тире. |
| ShortDot | `2` | Стиль системного тире. |
| ShortDashDot | `3` | Стиль системного тире. |
| ShortDashDotDot | `4` | Стиль системного тире. |
| Dot | `5` | Стиль квадратной точки. |
| Dash | `6` | Стиль штриха. |
| LongDash | `7` | Стиль длинного тире. |
| DashDot | `8` | Тире, короткое тире. |
| LongDashDot | `9` | Длинное тире, короткое тире. |
| LongDashDotDot | `10` | Длинное тире, короткое тире, короткое тире. |
| Default | `0` | То же, что иSolid . |

### Примеры

Показывает создание разнообразных фигур.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены четыре примера фигур, которые мы можем вставить в наши документы.
// 1 - Пунктирная горизонтальная полупрозрачная красная линия
// со стрелкой на левом конце и ромбом на правом конце:
Shape arrow = new Shape(doc, ShapeType.Line);
arrow.Width = 200;
arrow.Stroke.Color = Color.Red;
arrow.Stroke.StartArrowType = ArrowType.Arrow;
arrow.Stroke.StartArrowLength = ArrowLength.Long;
arrow.Stroke.StartArrowWidth = ArrowWidth.Wide;
arrow.Stroke.EndArrowType = ArrowType.Diamond;
arrow.Stroke.EndArrowLength = ArrowLength.Long;
arrow.Stroke.EndArrowWidth = ArrowWidth.Wide;
arrow.Stroke.DashStyle = DashStyle.Dash;
arrow.Stroke.Opacity = 0.5;

Assert.AreEqual(JoinStyle.Miter, arrow.Stroke.JoinStyle);

builder.InsertNode(arrow);

// 2 - Толстая черная диагональная линия с закругленными концами:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Стрелка с зеленой заливкой:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 — Стрелка с перевернутой ориентацией, заполненная логотипом Aspose:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Когда мы меняем ориентацию нашей стрелки, мы также переворачиваем изображение, которое содержит стрелка.
    // Переверните изображение в другую сторону, чтобы отменить это, прежде чем получить форму для его отображения.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Смотрите также

* property [DashStyle](../stroke/dashstyle/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


