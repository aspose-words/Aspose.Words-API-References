---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words para .NET
description: Descubre la propiedad GlowFormat Color para personalizar tus efectos de brillo. Define fácilmente colores vibrantes para un impacto visual impactante. El valor predeterminado es negro.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Obtiene o establece unColor objeto que representa el color para un efecto de brillo. El valor predeterminado esBlack .

```csharp
public Color Color { get; set; }
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

* class [GlowFormat](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
