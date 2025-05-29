---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words para .NET
description: Descubre la propiedad ShapeBase ShadowFormat para mejorar tus diseños con efectos de sombra personalizables. ¡Mejora tu atractivo visual hoy mismo!
type: docs
weight: 520
url: /es/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Obtiene el formato de sombra para la forma.

```csharp
public ShadowFormat ShadowFormat { get; }
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

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
