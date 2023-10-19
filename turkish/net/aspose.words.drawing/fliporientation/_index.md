---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.FlipOrientation Sıralama. Şeklin yönüne ilişkin olası değerler C#'da.
type: docs
weight: 970
url: /tr/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Şeklin yönüne ilişkin olası değerler.

```csharp
[Flags]
public enum FlipOrientation
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Koordinatlar çevrilmez. |
| Horizontal | `1` | X koordinatlarını tersine çevirerek y ekseni boyunca çevirin. |
| Vertical | `2` | Y koordinatlarını ters çevirerek x ekseni boyunca çevirin. |
| Both | `3` | Hem y hem de x ekseni boyunca çevirin. |

## Örnekler

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

* property [FlipOrientation](../shapebase/fliporientation/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
