---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.GradientVariant для настраиваемых градиентных заливок, улучшающих дизайн ваших документов с помощью ярких стилей.
type: docs
weight: 1340
url: /ru/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Указывает вариант градиентной заливки.

```csharp
public enum GradientVariant
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Вариант градиента «Нет». |
| Variant1 | `1` | Вариант градиента 1. |
| Variant2 | `2` | Вариант градиента 2. |
| Variant3 | `3` | Вариант градиента 3. |
| Variant4 | `4` | Вариант градиента 4. |

## Примечания

Соответствует четырем вариантам на вкладке «Градиент» в диалоговом окне «Эффекты заливки» в Word.

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
