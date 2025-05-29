---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words para .NET
description: Explora la clase Aspose.Words.Drawing.GlowFormat para mejorar tus documentos con impresionantes efectos de brillo. ¡Mejora tu diseño con opciones de formato únicas!
type: docs
weight: 1300
url: /es/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Representa el formato de brillo de un objeto.

```csharp
public class GlowFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Obtiene o establece unColor objeto que representa el color para un efecto de brillo. El valor predeterminado esBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Obtiene o establece un valor doble que representa la longitud del radio de un efecto de brillo en puntos (pt). El valor predeterminado es 0.0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Obtiene o establece el grado de transparencia del efecto de brillo como un valor entre 0.0 (opaco) y 1.0 (transparente). El valor predeterminado es 0.0. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Elimina`GlowFormat` del objeto padre. |

## Observaciones

Utilice el[`Glow`](../shapebase/glow/) propiedad para acceder a las propiedades de brillo de un objeto. No crea instancias de la`GlowFormat` clase directamente.

## Ejemplos

Muestra cómo interactuar con el efecto de forma brillante.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
