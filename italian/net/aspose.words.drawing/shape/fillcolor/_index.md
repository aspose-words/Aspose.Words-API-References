---
title: Shape.FillColor
second_title: Aspose.Words per .NET API Reference
description: Shape proprietà. Definisce il colore del pennello che riempie il percorso chiuso della forma.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Definisce il colore del pennello che riempie il percorso chiuso della forma.

```csharp
public Color FillColor { get; set; }
```

### Osservazioni

Questa è una scorciatoia per[`Color`](../../fill/color/) proprietà.

Il valore predefinito è White.

### Esempi

Mostra come riempire una forma con un colore a tinta unita.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Scrivi del testo e poi coprilo con una forma fluttuante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilizza la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape.StrokeColor = Color.CadetBlue;

// Utilizza la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape.FillColor = Color.LightBlue;

// La proprietà "Opacità" determina quanto trasparente è il colore su una scala 0-1,
// dove 1 è completamente opaco e 0 è invisibile.
// Il riempimento della forma per impostazione predefinita è completamente opaco, quindi non possiamo vedere il testo su cui si trova questa forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Imposta l'opacità del colore di riempimento della forma su un valore inferiore in modo da poter vedere il testo sottostante.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Guarda anche

* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shape/)
* assemblea [Aspose.Words](../../../)


