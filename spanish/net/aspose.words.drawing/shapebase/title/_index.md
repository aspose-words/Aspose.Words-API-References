---
title: ShapeBase.Title
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Obtiene o establece el título título del objeto de forma actual.
type: docs
weight: 490
url: /es/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Obtiene o establece el título (título) del objeto de forma actual.

```csharp
public string Title { get; set; }
```

### Observaciones

El valor predeterminado es una cadena vacía.

No puede ser nulo, pero puede ser una cadena vacía.

### Ejemplos

Muestra cómo establecer el título de una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree una forma, asígnele un título y luego agréguela al documento.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// Cuando guardamos un documento con una forma que tiene un título,
// Aspose.Words almacenará ese título en el texto alternativo de la forma.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


