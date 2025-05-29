---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words per .NET
description: Scopri la proprietà Stroke Color2: migliora i tuoi progetti con un secondo colore di tratto personalizzabile per ottenere effetti visivi vivaci e accattivanti.
type: docs
weight: 60
url: /it/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Definisce un secondo colore per un tratto.

```csharp
public Color Color2 { get; set; }
```

## Osservazioni

Il valore predefinito per a[`Shape`](../../shape/) è White .

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
