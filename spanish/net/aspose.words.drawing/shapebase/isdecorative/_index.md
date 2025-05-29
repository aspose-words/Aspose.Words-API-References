---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words para .NET
description: Descubra ShapeBase. Gestione fácilmente las propiedades decorativas de sus documentos. Mejore el atractivo visual configurando indicadores para diseños de formas únicos.
type: docs
weight: 260
url: /es/net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Obtiene o establece el indicador que especifica si la forma es decorativa en el documento.

```csharp
public bool IsDecorative { get; set; }
```

## Observaciones

Nótese que la forma no tiene espacio vacío[`AlternativeText`](../alternativetext/) no puede ser decorativo.

## Ejemplos

Muestra cómo configurar la forma para que sea decorativa.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(shape.IsDecorative);

// Si "Texto alternativo" no está vacío, la forma no puede ser decorativa.
// Es por eso que nuestro valor ha cambiado a 'falso'.
shape.AlternativeText = "Alternative text.";
Assert.False(shape.IsDecorative);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
//Crea una nueva forma como decorativa.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
