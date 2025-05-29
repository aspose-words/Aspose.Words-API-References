---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà ImageBytes per creare splendide immagini tratteggiate e riempimenti a motivo unici per i tuoi progetti. Migliora i tuoi effetti visivi oggi stesso!
type: docs
weight: 160
url: /it/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Definisce l'immagine per un'immagine di tratto o un riempimento a motivo.

```csharp
public byte[] ImageBytes { get; }
```

## Esempi

Mostra come elaborare le caratteristiche dei tratti di forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// I tratti possono avere due colori, utilizzati per creare un motivo definito da dati di immagini bicolore.
// I tratti con un solo colore non utilizzano la proprietà Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Guarda anche

* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
