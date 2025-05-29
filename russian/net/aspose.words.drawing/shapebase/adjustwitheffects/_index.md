---
title: ShapeBase.AdjustWithEffects
linktitle: AdjustWithEffects
articleTitle: AdjustWithEffects
second_title: Aspose.Words для .NET
description: Узнайте, как метод ShapeBase AdjustWithEffects улучшает исходный прямоугольник, добавляя границы эффекта и обеспечивая точные конечные значения прямоугольника.
type: docs
weight: 660
url: /ru/net/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method

Добавляет к исходному прямоугольнику значения степени эффекта и возвращает конечный прямоугольник.

```csharp
public RectangleF AdjustWithEffects(RectangleF source)
```

## Примеры

Показывает, как проверить, как границы фигуры зависят от эффектов фигуры.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Две формы идентичны по размерам и типу формы.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// Первая фигура не имеет эффектов, а вторая имеет тень и толстый контур.
// Эти эффекты увеличивают размер силуэта второй фигуры по сравнению с первой.
// Несмотря на то, что размер прямоугольника отображается, когда мы нажимаем на эти фигуры в Microsoft Word,
// видимые внешние границы второй фигуры подвержены влиянию тени и контура и поэтому больше.
// Мы можем использовать метод «AdjustWithEffects», чтобы увидеть истинный размер фигуры.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// Создаем объект RectangleF, представляющий прямоугольник,
// которые мы могли бы потенциально использовать в качестве координат и границ фигуры.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Запустите этот метод, чтобы скорректировать размер прямоугольника с учетом всех наших эффектов формы.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Поскольку форма не имеет эффектов изменения границ, ее граничные размеры не изменяются.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// Проверьте окончательный размер первой фигуры в точках.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Эффекты формы немного сместили видимый верхний левый угол фигуры.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// Эффекты также повлияли на видимые размеры фигуры.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1133.5, rectangleFOut.Height);

// Эффекты также затронули видимые границы фигуры.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(280.5, shape.BoundsWithEffects.Height);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
