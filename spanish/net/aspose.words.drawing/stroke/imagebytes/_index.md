---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words para .NET
description: Stroke ImageBytes propiedad. Define la imagen para una imagen de trazo o relleno de patrón en C#.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Define la imagen para una imagen de trazo o relleno de patrón.

```csharp
public byte[] ImageBytes { get; }
```

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
