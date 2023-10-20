---
title: Stroke.StartArrowType
linktitle: StartArrowType
articleTitle: StartArrowType
second_title: Aspose.Words per .NET
description: Stroke StartArrowType proprietà. Definisce la punta della freccia per linizio di un tratto in C#.
type: docs
weight: 170
url: /it/net/aspose.words.drawing/stroke/startarrowtype/
---
## Stroke.StartArrowType property

Definisce la punta della freccia per l'inizio di un tratto.

```csharp
public ArrowType StartArrowType { get; set; }
```

## Osservazioni

Il valore predefinito èNone.

## Esempi

Mostra per creare una varietà di forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati quattro esempi di forme che possiamo inserire nei nostri documenti.
// 1 - Linea rossa tratteggiata, orizzontale, semitrasparente
// con una freccia all'estremità sinistra e un diamante all'estremità destra:
Shape arrow = new Shape(doc, ShapeType.Line);
arrow.Width = 200;
arrow.Stroke.Color = Color.Red;
arrow.Stroke.StartArrowType = ArrowType.Arrow;
arrow.Stroke.StartArrowLength = ArrowLength.Long;
arrow.Stroke.StartArrowWidth = ArrowWidth.Wide;
arrow.Stroke.EndArrowType = ArrowType.Diamond;
arrow.Stroke.EndArrowLength = ArrowLength.Long;
arrow.Stroke.EndArrowWidth = ArrowWidth.Wide;
arrow.Stroke.DashStyle = DashStyle.Dash;
arrow.Stroke.Opacity = 0.5;

Assert.AreEqual(JoinStyle.Miter, arrow.Stroke.JoinStyle);

builder.InsertNode(arrow);

// 2 - Spessa linea diagonale nera con estremità arrotondate:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Freccia con riempimento verde:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Freccia con orientamento invertito riempito con il logo Aspose:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Quando invertiamo l'orientamento della nostra freccia, invertiamo anche l'immagine che la freccia contiene.
    // Capovolgi l'immagine nell'altro modo per annullarla prima di ottenere la forma per visualizzarla.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Guarda anche

* enum [ArrowType](../../arrowtype/)
* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
