---
title: NodeCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „NodeCollection ToArray“, konvertieren Sie Ihre Knotensammlung mühelos in ein neues Array und verbessern Sie so die Datenverwaltung und Zugänglichkeit.
type: docs
weight: 110
url: /de/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Kopiert alle Knoten aus der Sammlung in ein neues Knoten-Array.

```csharp
public Node[] ToArray()
```

### Rückgabewert

Ein Array von Knoten.

## Bemerkungen

Sie sollten keine Knoten hinzufügen/entfernen, während Sie über eine Sammlung von Knoten iterieren, da dies den Iterator ungültig macht und Aktualisierungen für Live-Sammlungen erforderlich macht.

Um während der Iteration Knoten hinzufügen/entfernen zu können, verwenden Sie diese Methode, um -Knoten in ein Array mit fester Größe zu kopieren und dann über das Array zu iterieren.

## Beispiele

Zeigt, wie alle Textfeldformen durch Bildformen ersetzt werden.

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

### Siehe auch

* class [Node](../../node/)
* class [NodeCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
