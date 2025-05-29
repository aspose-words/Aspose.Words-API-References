---
title: Fill.BackColor
linktitle: BackColor
articleTitle: BackColor
second_title: Aspose.Words для .NET
description: Легко настройте цвет фона заливки с помощью свойства BackColor. Легко установите или получите объект Color для яркого дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/fill/backcolor/
---
## Fill.BackColor property

Возвращает или задает объект Color, представляющий цвет фона для заливки.

```csharp
public Color BackColor { get; set; }
```

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

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
