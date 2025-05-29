---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: .NET için Aspose.Words
description: NoTextRotation özelliğiyle TextBox'ınızdaki metin dönüşünü kontrol edin. Şekiller döndürüldüğünde bile net, okunabilir metin sağlayın. Tasarımınızı geliştirin!
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Şekil döndürüldüğünde TextBox'ın metninin dönmemesi gerektiğini belirten bir Boole değeri alır veya ayarlar.

```csharp
public bool NoTextRotation { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`

## Örnekler

Şekil döndürüldüğünde metin döndürmenin nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Ayrıca bakınız

* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
