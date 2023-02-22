---
title: ShapeBase.WrapSide
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Specifica come il testo viene avvolto attorno alla forma.
type: docs
weight: 530
url: /it/net/aspose.words.drawing/shapebase/wrapside/
---
## ShapeBase.WrapSide property

Specifica come il testo viene avvolto attorno alla forma.

```csharp
public WrapSide WrapSide { get; set; }
```

### Osservazioni

Il valore predefinito èBoth.

Ha effetto solo per le forme di livello superiore.

### Esempi

Mostra come sostituire tutte le forme casella di testo con forme immagine.

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

### Guarda anche

* enum [WrapSide](../../wrapside/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


