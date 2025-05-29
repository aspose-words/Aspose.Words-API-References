---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Drawing.WrapSide för att styra textbrytning runt former och bilder, vilket förbättrar dokumentlayout och läsbarhet.
type: docs
weight: 1800
url: /sv/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Anger vilken/vilka sidor av formen eller bilden texten ska radbrytas runt.

```csharp
public enum WrapSide
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Both | `0` | Dokumenttexten radbryts på båda sidor av formen. |
| Left | `1` | Dokumentets text radbryts endast på vänster sida av formen. Det finns ett textfritt område till höger om formen. |
| Right | `2` | Dokumentets text radbryts endast på höger sida av formen. Det finns ett textfritt område på vänster sida av formen. |
| Largest | `3` | Dokumenttexten radbryts på den sida av formen som är längst bort från sidmarginalen, vilket lämnar ett textfritt område på den andra sidan av formen. |
| Default | `0` | Standardvärdet ärBoth . |

## Exempel

Visar hur man ersätter alla textruteformer med bildformer.

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

### Se även

* property [WrapSide](../shapebase/wrapside/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
