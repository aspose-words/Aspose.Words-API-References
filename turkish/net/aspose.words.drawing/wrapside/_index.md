---
title: Enum WrapSide
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.WrapSide Sıralama. Metnin şeklin veya resmin hangi tarafını/yanlarını sardığını belirtir.
type: docs
weight: 1240
url: /tr/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Metnin, şeklin veya resmin hangi tarafını/yanlarını sardığını belirtir.

```csharp
public enum WrapSide
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Both | `0` | Belge metni, şeklin her iki tarafına da sarılır. |
| Left | `1` | Belge metni, şeklin yalnızca sol tarafına kaydırılır. Şeklin sağ tarafında metin içermeyen bir alan var. |
| Right | `2` | Belge metni, şeklin yalnızca sağ tarafına kaydırılır. Şeklin sol tarafında metin içermeyen bir alan var. |
| Largest | `3` | Belge metni, şeklin sayfa kenar boşluğundan en uzak tarafına sarılarak şeklin diğer tarafında metinsiz alan bırakır. |
| Default | `0` | Varsayılan değerBoth . |

### Örnekler

Tüm metin kutusu şekillerinin görüntü şekilleriyle nasıl değiştirileceğini gösterir.

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


