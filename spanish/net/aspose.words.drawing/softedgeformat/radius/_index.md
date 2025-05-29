---
title: SoftEdgeFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words para .NET
description: Descubra la propiedad Radio de SoftEdgeFormat para ajustar fácilmente los efectos de bordes suaves. Controle la longitud del radio con precisión para obtener resultados visuales impresionantes.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/softedgeformat/radius/
---
## SoftEdgeFormat.Radius property

Obtiene o establece un valor doble que representa la longitud del radio para un efecto de borde suave en puntos (pt). El valor predeterminado es 0.0.

```csharp
public double Radius { get; set; }
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

* class [SoftEdgeFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
