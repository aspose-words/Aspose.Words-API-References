---
title: GlowFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo GlowFormat dal tuo oggetto padre con il nostro efficiente metodo GlowFormat Remove. Migliora il tuo flusso di lavoro di progettazione oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.drawing/glowformat/remove/
---
## GlowFormat.Remove method

Rimuove[`GlowFormat`](../) dall'oggetto padre.

```csharp
public void Remove()
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
