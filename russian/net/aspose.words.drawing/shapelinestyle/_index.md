---
title: Enum ShapeLineStyle
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.ShapeLineStyle перечисление. Определяет стиль составной линииShape .
type: docs
weight: 1120
url: /ru/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Определяет стиль составной линии[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Single | `0` | Одна строка. |
| Double | `1` | Двойные линии одинаковой ширины. |
| ThickThin | `2` | Двойные линии, одна толстая, другая тонкая. |
| ThinThick | `3` | Двойные линии, одна тонкая, другая толстая. |
| Triple | `4` | Три линии, тонкая, толстая, тонкая. |
| Default | `0` | Значение по умолчанию:Single . |

### Примеры

Показывает, как изменяются свойства обводки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Базовые фигуры, такие как прямоугольник, имеют две видимые части.
// 1 - Заливка, которая применяется к области внутри контура фигуры:
shape.Fill.ForeColor = Color.White;

// 2 - Обводка, обозначающая контур фигуры:
// Изменяем различные свойства обводки этой фигуры.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Смотрите также

* property [LineStyle](../stroke/linestyle/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


