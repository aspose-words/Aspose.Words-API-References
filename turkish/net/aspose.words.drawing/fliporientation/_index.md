---
title: Enum FlipOrientation
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.FlipOrientation Sıralama. Bir şeklin oryantasyonu için olası değerler.
type: docs
weight: 840
url: /tr/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Bir şeklin oryantasyonu için olası değerler.

```csharp
[Flags]
public enum FlipOrientation
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Koordinatlar çevrilmez. |
| Horizontal | `1` | x koordinatlarını tersine çevirerek y ekseni boyunca çevirin. |
| Vertical | `2` | y-koordinatlarını tersine çevirerek x ekseni boyunca çevirin. |
| Both | `3` | Hem y hem de x ekseni boyunca çevirin. |

### Örnekler

Bir eksende bir şeklin nasıl çevrileceğini gösterir.

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

// İkinci şekli y ekseninde çevirmek için "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayın,
// ilk şeklin yatay ayna görüntüsüne dönüştürüyoruz.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Üçüncü şekli x ekseninde çevirmek için "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayın,
// ilk şeklin dikey ayna görüntüsüne dönüştürüyoruz.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Dördüncü şekli hem x hem de y eksenlerinde çevirmek için "FlipOrientation" özelliğini "FlipOrientation.Horizontal" olarak ayarlayın,
// ilk şeklin yatay ve dikey ayna görüntüsüne dönüştürüyoruz.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Ayrıca bakınız

* property [FlipOrientation](../shapebase/fliporientation/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


