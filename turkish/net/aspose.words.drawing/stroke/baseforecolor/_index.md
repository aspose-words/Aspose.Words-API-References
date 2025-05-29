---
title: Stroke.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: .NET için Aspose.Words
description: Kesin tasarım kontrolü için konturunuzun değiştirilmemiş temel ön plan rengine kolayca erişmek üzere Stroke BaseForeColor özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/stroke/baseforecolor/
---
## Stroke.BaseForeColor property

Herhangi bir değiştirici kullanmadan vuruşun temel ön plan rengini alır.

```csharp
public Color BaseForeColor { get; }
```

## Notlar

Bir değer için varsayılan değer[`Shape`](../../shape/) x000d_ miBlack .

## Örnekler

Değiştirici kullanmadan ön plan renginin nasıl alınacağını gösterir.

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

### Ayrıca bakınız

* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
