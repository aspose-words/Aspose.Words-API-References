---
title: Stroke.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Stroke Fill для улучшенного форматирования заливки в ваших проектах. Поднимите свои проекты на новый уровень с помощью точной настройки штриха уже сегодня!
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/stroke/fill/
---
## Stroke.Fill property

Получает форматирование заполнения для[`Stroke`](../) .

```csharp
public Fill Fill { get; }
```

## Примеры

Показывает, как изменить свойства штриха.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Базовые фигуры, такие как прямоугольник, состоят из двух видимых частей.
// 1 — Заливка, которая применяется к области внутри контура фигуры:
shape.Fill.ForeColor = Color.White;

// 2 - Штрих, обозначающий контур фигуры:
// Измените различные свойства обводки этой фигуры.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Смотрите также

* class [Fill](../../fill/)
* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
