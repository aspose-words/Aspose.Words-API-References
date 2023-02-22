---
title: ShapeBase.Rotation
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin döndürüldüğü açıyı derece olarak tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir.
type: docs
weight: 430
url: /tr/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Şeklin döndürüldüğü açıyı (derece olarak) tanımlar. Pozitif değer, saat yönünde dönüş açısına karşılık gelir.

```csharp
public double Rotation { get; set; }
```

### Notlar

Varsayılan değer 0'dır.

### Örnekler

Bir görüntünün nasıl ekleneceğini ve döndürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Resim içeren bir şekil ekleyin.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Resmi saat yönünde 45 derece döndür.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


