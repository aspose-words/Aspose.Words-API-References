---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Drawing.GlowFormat per arricchire i tuoi documenti con straordinari effetti di luminosità. Valorizza il tuo design con opzioni di formattazione uniche!
type: docs
weight: 1300
url: /it/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Rappresenta la formattazione luminosa per un oggetto.

```csharp
public class GlowFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Ottiene o imposta unColor oggetto che rappresenta il colore per un effetto bagliore. Il valore predefinito èBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Ottiene o imposta un valore double che rappresenta la lunghezza del raggio per un effetto bagliore in punti (pt). Il valore predefinito è 0.0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Ottiene o imposta il grado di trasparenza per l'effetto bagliore come valore compreso tra 0,0 (opaco) e 1,0 (trasparente). Il valore predefinito è 0,0. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Rimuove`GlowFormat` dall'oggetto padre. |

## Osservazioni

Utilizzare il[`Glow`](../shapebase/glow/) proprietà per accedere alle proprietà di luminosità di un oggetto. Non si creano istanze di`GlowFormat` classe direttamente.

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
