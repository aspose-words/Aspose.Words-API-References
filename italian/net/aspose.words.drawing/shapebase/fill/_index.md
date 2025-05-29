---
title: ShapeBase.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words per .NET
description: Scopri la proprietà Riempimento ShapeBase per migliorare i tuoi progetti con una formattazione di riempimento personalizzabile per le forme. Migliora i tuoi effetti visivi senza sforzo!
type: docs
weight: 170
url: /it/net/aspose.words.drawing/shapebase/fill/
---
## ShapeBase.Fill property

Ottiene la formattazione di riempimento per la forma.

```csharp
public Fill Fill { get; }
```

## Esempi

Mostra come riempire una forma con un colore pieno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Scrivi del testo e poi coprilo con una forma fluttuante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilizzare la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape.StrokeColor = Color.CadetBlue;

// Utilizzare la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape.FillColor = Color.LightBlue;

// La proprietà "Opacità" determina quanto è trasparente il colore su una scala da 0 a 1,
// dove 1 è completamente opaco e 0 è invisibile.
// Per impostazione predefinita, il riempimento della forma è completamente opaco, quindi non possiamo vedere il testo su cui si trova questa forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Imposta l'opacità del colore di riempimento della forma su un valore più basso, in modo da poter vedere il testo sottostante.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Guarda anche

* class [Fill](../../fill/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
