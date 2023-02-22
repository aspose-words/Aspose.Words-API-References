---
title: ShapeBase.SizeInPoints
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin boyutunu nokta olarak alır.
type: docs
weight: 470
url: /tr/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Şeklin boyutunu nokta olarak alır.

```csharp
public SizeF SizeInPoints { get; }
```

### Örnekler

Bir şeklin boyutunun ve işaretleme dilinin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


