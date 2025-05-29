---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: .NET için Aspose.Words
description: Hassas tasarım kontrolü için şekil boyutlarını noktalar halinde kolayca almak ve yönetmek amacıyla ShapeBase SizeInPoints özelliğini keşfedin.
type: docs
weight: 540
url: /tr/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Şeklin boyutunu noktalar halinde alır.

```csharp
public SizeF SizeInPoints { get; }
```

## Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
