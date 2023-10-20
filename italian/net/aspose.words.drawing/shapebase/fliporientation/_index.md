---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words per .NET
description: ShapeBase FlipOrientation proprietà. Cambia lorientamento di una forma in C#.
type: docs
weight: 180
url: /it/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Cambia l'orientamento di una forma.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Osservazioni

Il valore predefinito èNone.

## Esempi

Mostra come capovolgere una forma su un asse.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma di immagine e lascia il suo orientamento nel suo stato predefinito.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "FlipOrientation" su "FlipOrientation.Horizontal" per capovolgere la seconda forma sull'asse y,
// trasformandolo in un'immagine speculare orizzontale della prima forma.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "FlipOrientation" su "FlipOrientation.Horizontal" per capovolgere la terza forma sull'asse x,
// trasformandolo in un'immagine speculare verticale della prima forma.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "FlipOrientation" su "FlipOrientation.Horizontal" per invertire la quarta forma su entrambi gli assi x e y,
// trasformandolo in un'immagine speculare orizzontale e verticale della prima forma.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Guarda anche

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
