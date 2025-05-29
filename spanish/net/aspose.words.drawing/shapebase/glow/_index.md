---
title: ShapeBase.Glow
linktitle: Glow
articleTitle: Glow
second_title: Aspose.Words para .NET
description: ¡Mejora tus diseños con ShapeBase Glow! Consigue efectos de brillo impresionantes para tus formas y realza tus proyectos visuales sin esfuerzo.
type: docs
weight: 200
url: /es/net/aspose.words.drawing/shapebase/glow/
---
## ShapeBase.Glow property

Obtiene formato de brillo para la forma.

```csharp
public GlowFormat Glow { get; }
```

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

* class [GlowFormat](../../glowformat/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
