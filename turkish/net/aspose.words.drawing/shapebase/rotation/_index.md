---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: .NET için Aspose.Words
description: ShapeBase Rotation özelliğini keşfedin, şekilleriniz için dönüş açılarını kolayca tanımlayın ve özelleştirin, tasarımınızın hassasiyetini ve yaratıcılığını artırın.
type: docs
weight: 500
url: /tr/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Bir şeklin döndürüleceği açıyı (derece olarak) tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir.

```csharp
public double Rotation { get; set; }
```

## Notlar

Varsayılan değer 0'dır.

## Örnekler

Bir resmin nasıl ekleneceğini ve döndürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resimli bir şekil ekle.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Görüntüyü saat yönünde 45 derece döndür.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
