---
title: ShapeBase.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase DistanceRight e regola facilmente la spaziatura in punti tra il testo del documento e il bordo destro di una forma per un controllo migliorato del layout.
type: docs
weight: 150
url: /it/net/aspose.words.drawing/shapebase/distanceright/
---
## ShapeBase.DistanceRight property

Restituisce o imposta la distanza (in punti) tra il testo del documento e il bordo destro della forma.

```csharp
public double DistanceRight { get; set; }
```

## Osservazioni

Il valore predefinito è 1/8 di pollice.

Ha effetto solo sulle forme di livello superiore.

## Esempi

Mostra come impostare la distanza di avvolgimento di un testo che circonda una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un rettangolo e fa sì che il testo si adatti strettamente ai suoi limiti.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Imposta la distanza minima tra la forma e il testo circostante a 40 pt da tutti i lati.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Sposta la forma più vicino al centro della pagina, quindi ruotala di 60 gradi in senso orario.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

// Aggiungere il testo che circonderà la forma.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
