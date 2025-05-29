---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.FlipOrientation per opzioni di orientamento delle forme versatili. Migliora il design dei tuoi documenti con una personalizzazione flessibile!
type: docs
weight: 1290
url: /it/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Valori possibili per l'orientamento di una forma.

```csharp
[Flags]
public enum FlipOrientation
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Le coordinate non sono invertite. |
| Horizontal | `1` | Capovolgi lungo l'asse y, invertendo le coordinate x. |
| Vertical | `2` | Capovolgi lungo l'asse x, invertendo le coordinate y. |
| Both | `3` | Capovolgi sia lungo l'asse y che lungo l'asse x. |

## Esempi

Mostra come capovolgere una forma su un asse.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce una forma immagine e lascia il suo orientamento nello stato predefinito.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "FlipOrientation" su "FlipOrientation.Horizontal" per capovolgere la seconda forma sull'asse y,
// trasformandola in un'immagine speculare orizzontale della prima forma.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "FlipOrientation" su "FlipOrientation.Horizontal" per capovolgere la terza forma sull'asse x,
// trasformandola in un'immagine speculare verticale della prima forma.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Imposta la proprietà "FlipOrientation" su "FlipOrientation.Horizontal" per capovolgere la quarta forma sia sull'asse x che sull'asse y,
// trasformandola in un'immagine speculare orizzontale e verticale della prima forma.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Guarda anche

* property [FlipOrientation](../shapebase/fliporientation/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
