---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words per .NET
description: Scopri la proprietà GlowFormat Color per personalizzare i tuoi effetti di bagliore. Imposta facilmente colori vivaci per un impatto visivo straordinario. L'impostazione predefinita è Nero.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Ottiene o imposta unColor oggetto che rappresenta il colore per un effetto bagliore. Il valore predefinito èBlack .

```csharp
public Color Color { get; set; }
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
