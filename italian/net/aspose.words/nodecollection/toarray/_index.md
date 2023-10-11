---
title: NodeCollection.ToArray
second_title: Aspose.Words per .NET API Reference
description: NodeCollection metodo. Copia tutti i nodi dalla raccolta in un nuovo array di nodi.
type: docs
weight: 110
url: /it/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Copia tutti i nodi dalla raccolta in un nuovo array di nodi.

```csharp
public Node[] ToArray()
```

### Valore di ritorno

Una matrice di nodi.

### Osservazioni

Non dovresti aggiungere/rimuovere nodi durante l'iterazione su una raccolta di nodi perché invalida l'iteratore e richiede aggiornamenti per le raccolte attive.

Per poter aggiungere/rimuovere nodi durante l'iterazione, utilizzare questo metodo per copiare i nodi in un array di dimensioni fisse e quindi scorrere l'array.

### Esempi

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

* class [Node](../../node/)
* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../nodecollection/)
* assemblea [Aspose.Words](../../../)


