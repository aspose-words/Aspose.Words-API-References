---
title: GlowFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words per .NET
description: Scopri la proprietà GlowFormat Radius per personalizzare i tuoi effetti di bagliore. Regola il raggio in punti per ottenere straordinari miglioramenti visivi. Valore predefinito: 0,0.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/glowformat/radius/
---
## GlowFormat.Radius property

Ottiene o imposta un valore double che rappresenta la lunghezza del raggio per un effetto bagliore in punti (pt). Il valore predefinito è 0.0.

```csharp
public double Radius { get; set; }
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
