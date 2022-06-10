---
title: TwoColorGradient
second_title: Справочник по API Aspose.Words для .NET
description: Устанавливает для указанной заливки двухцветный градиент.
type: docs
weight: 210
url: /ru/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(GradientStyle, GradientVariant) {#twocolorgradient}

Устанавливает для указанной заливки двухцветный градиент.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | GradientStyle | Стиль градиента[`GradientStyle`](../../gradientstyle). |
| variant | GradientVariant | Вариант градиента[`GradientVariant`](../../gradientvariant) |

### Примеры

Показывает, как заполнить фигуру градиентами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применяем одноцветную градиентную заливку к фигуре с ForeColor градиентной заливки.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применяем к фигуре заливку двухцветным градиентом.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Изменяем BackColor градиентной заливки.
shape.Fill.BackColor = Color.Yellow;
// Обратите внимание, что "GradientAngle" заменяется на "GradientStyle.FromCorner/GradientStyle.FromCenter"
// градиентная заливка не дает никакого эффекта, она будет работать только для линейного градиента.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Используйте параметр соответствия для определения формы с помощью DML, если вы хотите получить "GradientStyle",
// Свойства "GradientVariant" и "GradientAngle" после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Смотрите также

* enum [GradientStyle](../../gradientstyle)
* enum [GradientVariant](../../gradientvariant)
* class [Fill](../../fill)
* пространство имен [Aspose.Words.Drawing](../../fill)
* сборка [Aspose.Words](../../../)

---

## TwoColorGradient(Color, Color, GradientStyle, GradientVariant) {#twocolorgradient_1}

Устанавливает для указанной заливки двухцветный градиент.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| color1 | Color | Первый цвет для построения градиента. |
| color2 | Color | Второй цвет для построения градиента. |
| style | GradientStyle | Стиль градиента[`GradientStyle`](../../gradientstyle). |
| variant | GradientVariant | Вариант градиента[`GradientVariant`](../../gradientvariant) |

### Примеры

Показывает, как заполнить фигуру градиентами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применяем одноцветную градиентную заливку к фигуре с ForeColor градиентной заливки.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Применяем к фигуре заливку двухцветным градиентом.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Изменяем BackColor градиентной заливки.
shape.Fill.BackColor = Color.Yellow;
// Обратите внимание, что "GradientAngle" заменяется на "GradientStyle.FromCorner/GradientStyle.FromCenter"
// градиентная заливка не дает никакого эффекта, она будет работать только для линейного градиента.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Используйте параметр соответствия для определения формы с помощью DML, если вы хотите получить "GradientStyle",
// Свойства "GradientVariant" и "GradientAngle" после сохранения документа.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Смотрите также

* enum [GradientStyle](../../gradientstyle)
* enum [GradientVariant](../../gradientvariant)
* class [Fill](../../fill)
* пространство имен [Aspose.Words.Drawing](../../fill)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
