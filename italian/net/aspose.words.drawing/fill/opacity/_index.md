---
title: Fill.Opacity
linktitle: Opacity
articleTitle: Opacity
second_title: Aspose.Words per .NET
description: Controlla la trasparenza del tuo design con la proprietà Opacità riempimento, regolando la nitidezza da completamente trasparente a completamente opaca per ottenere effetti visivi sorprendenti.
type: docs
weight: 150
url: /it/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Ottiene o imposta il grado di opacità del riempimento specificato come valore compreso tra 0,0 (trasparente) e 1,0 (opaco).

```csharp
public double Opacity { get; set; }
```

## Osservazioni

Questa proprietà è l'opposto della proprietà[`Transparency`](../transparency/).

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

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
