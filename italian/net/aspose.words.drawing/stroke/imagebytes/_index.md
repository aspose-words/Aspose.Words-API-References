---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words per .NET
description: Stroke ImageBytes proprietà. Definisce limmagine per unimmagine di tratto o un riempimento a motivo in C#.
type: docs
weight: 110
url: /it/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Definisce l'immagine per un'immagine di tratto o un riempimento a motivo.

```csharp
public byte[] ImageBytes { get; }
```

## Esempi

Mostra come elaborare le funzionalità del tratto forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// I tratti possono avere due colori, che vengono utilizzati per creare un motivo definito da dati immagine bicolore.
// I tratti con un singolo colore non utilizzano la proprietà Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Guarda anche

* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
