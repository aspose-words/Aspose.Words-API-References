---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words para .NET
description: Stroke Color2 propiedad. Define un segundo color para un trazo en C#.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Define un segundo color para un trazo.

```csharp
public Color Color2 { get; set; }
```

## Observaciones

El valor predeterminado para un[`Shape`](../../shape/) es White.

## Ejemplos

Muestra cómo procesar características de trazo de forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Los trazos pueden tener dos colores, que se utilizan para crear un patrón definido por datos de imagen de dos tonos.
// Los trazos de un solo color no utilizan la propiedad Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Ver también

* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
