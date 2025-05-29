---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.SoftEdgeFormat para mejorar sus documentos con impresionantes efectos de bordes suaves para una apariencia profesional.
type: docs
weight: 1710
url: /es/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Representa el formato de borde suave para un objeto.

```csharp
public class SoftEdgeFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Obtiene o establece un valor doble que representa la longitud del radio para un efecto de borde suave en puntos (pt). El valor predeterminado es 0.0. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Elimina`SoftEdgeFormat` del objeto padre. |

## Observaciones

Utilice el[`SoftEdge`](../shapebase/softedge/) propiedad para acceder a las propiedades del borde suave de un objeto. No crea instancias de la`SoftEdgeFormat` clase directamente.

## Ejemplos

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
