---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.WrapSide enum. Specifica su quali lati della forma o dellimmagine si avvolge il testo in C#.
type: docs
weight: 1390
url: /it/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Specifica su quali lati della forma o dell'immagine si avvolge il testo.

```csharp
public enum WrapSide
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Both | `0` | Il testo del documento viene disposto su entrambi i lati della forma. |
| Left | `1` | Il testo del documento va a capo solo sul lato sinistro della forma. C'è un'area libera da testo a destra della forma. |
| Right | `2` | Il testo del documento va a capo solo sul lato destro della forma. C'è un'area libera da testo sul lato sinistro della forma. |
| Largest | `3` | Il testo del documento va a capo sul lato della forma più lontano dal margine della pagina, lasciando un'area libera di testo sull'altro lato della forma. |
| Default | `0` | Il valore predefinito èBoth . |

## Esempi

Mostra come sostituire tutte le forme delle caselle di testo con forme di immagine.

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

* property [WrapSide](../shapebase/wrapside/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
