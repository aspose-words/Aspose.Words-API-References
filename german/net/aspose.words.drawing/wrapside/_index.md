---
title: Enum WrapSide
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.WrapSide opsomming. Gibt an um welche Seiten der Form oder des Bildes sich der Text windet.
type: docs
weight: 1240
url: /de/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Gibt an, um welche Seite(n) der Form oder des Bildes sich der Text windet.

```csharp
public enum WrapSide
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Both | `0` | Der Dokumenttext wird auf beiden Seiten der Form umbrochen. |
| Left | `1` | Der Dokumenttext wird nur auf der linken Seite der Form umbrochen. Rechts neben der Form befindet sich ein textfreier Bereich. |
| Right | `2` | Der Dokumententext wird nur auf der rechten Seite der Form umbrochen. Auf der linken Seite der Form befindet sich ein textfreier Bereich. |
| Largest | `3` | Der Dokumenttext wird auf der Seite der Form umgebrochen, die am weitesten vom Seitenrand entfernt ist, sodass auf der anderen Seite der Form ein freier Textbereich bleibt. |
| Default | `0` | Standardwert istBoth . |

### Beispiele

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

* property [WrapSide](../shapebase/wrapside/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


