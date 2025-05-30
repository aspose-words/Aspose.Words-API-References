---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words para .NET
description: Descubra la propiedad Transparencia de GlowFormat y ajuste fácilmente los efectos de brillo de opaco a transparente (0.0 a 1.0) para un impacto visual impresionante. Valor predeterminado 0.0.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Obtiene o establece el grado de transparencia del efecto de brillo como un valor entre 0.0 (opaco) y 1.0 (transparente). El valor predeterminado es 0.0.

```csharp
public double Transparency { get; set; }
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
