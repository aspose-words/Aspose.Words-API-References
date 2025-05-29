---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words para .NET
description: Mejora tus diseños con ShapeBase SoftEdge para un formato de bordes suaves y uniformes. ¡Mejora tus imágenes sin esfuerzo y destaca en cada proyecto!
type: docs
weight: 550
url: /es/net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

Obtiene formato de borde suave para la forma.

```csharp
public SoftEdgeFormat SoftEdge { get; }
```

## Ejemplos

Muestra cómo establecer un límite para la resolución de la imagen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Muestra cómo trabajar con formato de bordes suaves.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Aplicar borde suave a la forma.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

//Cargar documento con forma de rectángulo con borde suave.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Verifique el radio del borde suave.
Assert.AreEqual(30, softEdgeFormat.Radius);

//Eliminar el borde suave de la forma.
softEdgeFormat.Remove();

// Verifique el radio del borde suave eliminado.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Ver también

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
