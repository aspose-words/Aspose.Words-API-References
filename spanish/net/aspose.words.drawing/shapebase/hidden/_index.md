---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words para .NET
description: Controla la visibilidad de las formas con la propiedad oculta de ShapeBase. Alterne fácilmente entre visible y oculto para una mayor flexibilidad de diseño.
type: docs
weight: 230
url: /es/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Obtiene o establece un valor booleano que indica si la forma es visible.

```csharp
public bool Hidden { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra cómo ocultar la forma.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
