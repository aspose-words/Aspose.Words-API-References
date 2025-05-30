---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words per .NET
description: Scopri la proprietà Trasparenza di GlowFormat e regola facilmente gli effetti di luminosità da opachi a trasparenti (da 0,0 a 1,0) per un impatto visivo sorprendente. Valore predefinito 0,0.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Ottiene o imposta il grado di trasparenza per l'effetto bagliore come valore compreso tra 0,0 (opaco) e 1,0 (trasparente). Il valore predefinito è 0,0.

```csharp
public double Transparency { get; set; }
```

## Esempi

Mostra come interagire con l'effetto forma luminosa.

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

### Guarda anche

* class [GlowFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
