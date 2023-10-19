---
title: NodeCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words for .NET
description: NodeCollection ToArray yöntem. Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar.

```csharp
public Node[] ToArray()
```

### Geri dönüş değeri

Bir dizi düğüm.

## Notlar

Yineleyiciyi geçersiz kıldığından ve canlı koleksiyonlar için yenilemeler gerektirdiğinden, düğüm koleksiyonu üzerinde yineleme yaparken düğüm eklememeli/kaldırmamalısınız.

Yineleme sırasında düğümleri ekleyebilmek/kaldırabilmek için, düğümlerini sabit boyutlu bir diziye kopyalamak ve ardından dizi üzerinde yineleme yapmak için bu yöntemi kullanın.

## Örnekler

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

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
