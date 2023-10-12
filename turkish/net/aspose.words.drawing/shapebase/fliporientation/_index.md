---
title: ShapeBase.FlipOrientation
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin yönünü değiştirir.
type: docs
weight: 180
url: /tr/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Şeklin yönünü değiştirir.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

### Notlar

Varsayılan değer:None.

### Örnekler

Bir şeklin eksen üzerinde nasıl çevrileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir görüntü şekli ekleyin ve yönünü varsayılan durumunda bırakın.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Y eksenindeki ikinci şekli çevirmek için "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayın,
// onu ilk şeklin yatay ayna görüntüsüne dönüştürüyoruz.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// X eksenindeki üçüncü şekli çevirmek için "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayın,
// onu ilk şeklin dikey ayna görüntüsüne dönüştürüyoruz.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Dördüncü şekli hem x hem de y ekseninde çevirmek için "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayın,
// onu ilk şeklin yatay ve dikey ayna görüntüsüne dönüştürüyoruz.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Ayrıca bakınız

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


