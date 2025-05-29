---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: .NET için Aspose.Words
description: Gelişmiş grafik nesne yönetimi için ShapeBase MarkupLanguage özelliğini keşfedin. Bugün kusursuz entegrasyonun ve gelişmiş tasarım verimliliğinin kilidini açın!
type: docs
weight: 410
url: /tr/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Bu grafik nesnesi için kullanılan MarkupLanguage'ı alır.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
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

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
