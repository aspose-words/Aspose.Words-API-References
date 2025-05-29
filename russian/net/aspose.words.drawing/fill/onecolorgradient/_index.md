---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words для .NET
description: Узнайте, как использовать метод OneColorGradient для создания потрясающих одноцветных градиентов для ваших проектов. Улучшайте свои проекты без усилий!
type: docs
weight: 220
url: /ru/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

Устанавливает указанную заливку в виде одноцветного градиента.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | GradientStyle | Градиентный стиль[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | Градиентный вариант[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Степень градиента. Может иметь значение от 0,0 (темный) до 1,0 (светлый). |

## Примеры

Показывает, как заполнить фигуру градиентом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применить одноцветную градиентную заливку к фигуре с помощью ForeColor градиентной заливки.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применить к фигуре двухцветную градиентную заливку.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Изменить BackColor градиентной заливки.
shape.Fill.BackColor = Color.Yellow;
// Обратите внимание, что "GradientAngle" меняется на "GradientStyle.FromCorner/GradientStyle.FromCenter"
// градиентная заливка не даст никакого эффекта, она будет работать только для линейного градиента.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Используйте параметр соответствия, чтобы определить форму с помощью DML, если вы хотите получить "GradientStyle",
// Свойства "GradientVariant" и "GradientAngle" после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Смотрите также

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)

---

## OneColorGradient(*Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient_1}

Устанавливает указанную заливку в виде одноцветного градиента, используя указанный цвет.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| color | Color | Цвет для построения градиента. |
| style | GradientStyle | Градиентный стиль[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | Градиентный вариант[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Степень градиента. Может иметь значение от 0,0 (темный) до 1,0 (светлый). |

## Примеры

Показывает, как заполнить фигуру градиентом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применить одноцветную градиентную заливку к фигуре с помощью ForeColor градиентной заливки.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применить к фигуре двухцветную градиентную заливку.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Изменить BackColor градиентной заливки.
shape.Fill.BackColor = Color.Yellow;
// Обратите внимание, что "GradientAngle" меняется на "GradientStyle.FromCorner/GradientStyle.FromCenter"
// градиентная заливка не даст никакого эффекта, она будет работать только для линейного градиента.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Используйте параметр соответствия, чтобы определить форму с помощью DML, если вы хотите получить "GradientStyle",
// Свойства "GradientVariant" и "GradientAngle" после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Смотрите также

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
