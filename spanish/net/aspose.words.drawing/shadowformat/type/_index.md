---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Explora la propiedad Tipo de Formato de Sombra para personalizar fácilmente tus efectos de sombra. Obtén o configura el Tipo de Sombra para una mayor flexibilidad de diseño.
type: docs
weight: 20
url: /es/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Obtiene o establece el valor especificado[`ShadowType`](../../shadowtype/) para ShadowFormat.

```csharp
public ShadowType Type { get; set; }
```

## Ejemplos

Muestra cómo obtener el color de la sombra.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Ver también

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
