---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words para .NET
description: Descubre la propiedad Color de FormatoSombra para personalizar los colores de las sombras en tus diseños. El valor predeterminado es negro, pero ¡da rienda suelta a tu creatividad con opciones vibrantes!
type: docs
weight: 10
url: /es/net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Obtiene unColor objeto que representa el color de la sombra. El valor predeterminado esBlack .

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
