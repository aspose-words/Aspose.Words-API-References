---
title: EndCap Enum
linktitle: EndCap
articleTitle: EndCap
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.EndCap для настраиваемых стилей концов строк. Улучшите дизайн своих документов уникальными визуальными эффектами!
type: docs
weight: 1260
url: /ru/net/aspose.words.drawing/endcap/
---
## EndCap enumeration

Задает стиль окончания строки.

```csharp
public enum EndCap
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Round | `0` | Закругленные концы. |
| Square | `1` | Квадрат выступает на половину ширины линии. |
| Flat | `2` | Линия заканчивается в конечной точке. |
| Default | `2` | Значение по умолчанию:Flat . |

## Примеры

Демонстрирует создание разнообразных фигур.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены четыре примера фигур, которые мы можем вставить в наши документы.
// 1 - Пунктирная, горизонтальная, полупрозрачная красная линия
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
    // Когда мы меняем ориентацию нашей стрелки, мы также меняем изображение, которое содержит стрелка.
    // Переверните изображение в другую сторону, чтобы устранить это, прежде чем получить форму для его отображения.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Смотрите также

* property [EndCap](../stroke/endcap/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
