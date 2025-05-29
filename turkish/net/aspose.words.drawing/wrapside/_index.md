---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: .NET için Aspose.Words
description: Şekillerin ve resimlerin etrafındaki metin kaydırmayı kontrol etmek, belge düzenini ve okunabilirliği geliştirmek için Aspose.Words.Drawing.WrapSide enum'unu keşfedin.
type: docs
weight: 1800
url: /tr/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Metnin şeklin veya resmin hangi tarafını/taraflarını saracağını belirtir.

```csharp
public enum WrapSide
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Both | `0` | Belge metni şeklin her iki tarafına da sarılır. |
| Left | `1` | Belge metni yalnızca şeklin sol tarafına sarılır. Şeklin sağında metinsiz bir alan vardır. |
| Right | `2` | Belge metni yalnızca şeklin sağ tarafına sarılır. Şeklin sol tarafında metinsiz bir alan vardır. |
| Largest | `3` | Belge metni, şeklin sayfa kenar boşluğundan en uzaktaki tarafına sarılır ve şeklin diğer tarafında metin için boş alan bırakır. |
| Default | `0` | Varsayılan değerBoth . |

## Örnekler

Tüm metin kutusu şekillerinin resim şekilleriyle nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Ayrıca bakınız

* property [WrapSide](../shapebase/wrapside/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
