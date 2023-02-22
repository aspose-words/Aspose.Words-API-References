---
title: ShapeBase.MarkupLanguage
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Bu grafik nesnesi için kullanılan İşaretleme Dilini alır.
type: docs
weight: 370
url: /tr/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Bu grafik nesnesi için kullanılan İşaretleme Dilini alır.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
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

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


