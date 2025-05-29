---
title: Stroke.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Stroke BaseForeColor, чтобы легко получить доступ к неизмененному базовому цвету переднего плана вашей обводки для точного управления дизайном.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/stroke/baseforecolor/
---
## Stroke.BaseForeColor property

Получает базовый цвет переднего плана обводки без каких-либо модификаторов.

```csharp
public Color BaseForeColor { get; }
```

## Примечания

Значение по умолчанию для[`Shape`](../../shape/) is Black .

## Примеры

Показывает, как получить цвет переднего плана без модификаторов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
shape.Fill.ForeColor = Color.Red;
shape.Fill.ForeTintAndShade = 0.5;
shape.Stroke.Fill.ForeColor = Color.Green;
shape.Stroke.Fill.Transparency = 0.5;

Assert.AreEqual(Color.FromArgb(255, 255, 188, 188).ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.BaseForeColor.ToArgb());

Assert.AreEqual(Color.FromArgb(128, 0, 128, 0).ToArgb(), shape.Stroke.ForeColor.ToArgb());
Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.BaseForeColor.ToArgb());

Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.Fill.ForeColor.ToArgb());
Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.Fill.BaseForeColor.ToArgb());
```

### Смотрите также

* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
