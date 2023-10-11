---
title: ShapeBase.DistanceTop
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Restituisce o imposta la distanza in punti tra il testo del documento e il bordo superiore della forma.
type: docs
weight: 160
url: /it/net/aspose.words.drawing/shapebase/distancetop/
---
## ShapeBase.DistanceTop property

Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo superiore della forma.

```csharp
public double DistanceTop { get; set; }
```

### Osservazioni

Il valore predefinito è 0.

Ha effetto solo per le forme di livello superiore.

### Esempi

Mostra come impostare la distanza di avvolgimento per un testo che circonda una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un rettangolo e fai in modo che il testo si avvolga strettamente attorno ai suoi limiti.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Imposta la distanza minima tra la forma e il testo circostante su 40pt da tutti i lati.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Sposta la forma più vicino al centro della pagina, quindi ruota la forma di 60 gradi in senso orario.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// Aggiungi testo che avvolgerà la forma.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


