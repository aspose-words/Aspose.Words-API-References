---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words para .NET
description: ShapeBase IsDeleteRevision propiedad. Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C#.
type: docs
weight: 250
url: /es/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsDeleteRevision { get; }
```

## Ejemplos

Muestra cómo trabajar con formas de revisión.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Inserta una forma en línea sin realizar seguimiento de revisiones, lo que hará que esta forma no sea una revisión de ningún tipo.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Comience a rastrear revisiones y luego inserte otra forma, que será una revisión.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Dado que eliminamos esa forma mientras seguíamos los cambios,
// la forma persiste en el documento y cuenta como una revisión eliminada.
// Aceptar esta revisión eliminará la forma permanentemente y rechazarla la mantendrá en el documento.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// E insertamos otra forma mientras realizamos el seguimiento de los cambios, por lo que esa forma contará como una revisión de inserción.
// Aceptar esta revisión asimilará esta forma en el documento como una no revisión,
// y rechazar la revisión eliminará esta forma permanentemente.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
