---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words para .NET
description: ShapeBase IsDecorative propiedad. Obtiene o establece la bandera que especifica si la forma es decorativa en el documento en C#.
type: docs
weight: 240
url: /es/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Obtiene o establece la bandera que especifica si la forma es decorativa en el documento.

```csharp
public bool IsDecorative { get; set; }
```

## Observaciones

Tenga en cuenta que la forma no está vacía[`AlternativeText`](../alternativetext/) no puede ser decorativo.

## Ejemplos

Muestra cómo configurar que la forma sea decorativa.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape) doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Si "AlternativeText" no está vacío, la forma no puede ser decorativa.
// Es por eso que nuestro valor ha cambiado a 'falso'.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Crea una nueva forma como decorativa.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
