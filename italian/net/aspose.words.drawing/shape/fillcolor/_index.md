---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà Shape FillColor per personalizzare i tuoi progetti con colori di pennello vivaci che esaltano le tue forme e valorizzano i tuoi progetti.
type: docs
weight: 50
url: /it/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Definisce il colore del pennello che riempie il tracciato chiuso della forma.

```csharp
public Color FillColor { get; set; }
```

## Osservazioni

Questa è una scorciatoia per[`Color`](../../fill/color/) proprietà.

Il valore predefinito è White .

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

* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
