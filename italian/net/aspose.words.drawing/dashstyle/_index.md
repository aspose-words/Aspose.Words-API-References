---
title: DashStyle Enum
linktitle: DashStyle
articleTitle: DashStyle
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.DashStyle per stili di linea tratteggiata versatili. Migliora il design dei tuoi documenti con elementi visivi personalizzabili.
type: docs
weight: 1250
url: /it/net/aspose.words.drawing/dashstyle/
---
## DashStyle enumeration

Stile linea tratteggiata.

```csharp
public enum DashStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Solid | `0` | Penna continua. |
| ShortDash | `1` | Stile del trattino di sistema. |
| ShortDot | `2` | Stile del trattino di sistema. |
| ShortDashDot | `3` | Stile del trattino di sistema. |
| ShortDashDotDot | `4` | Stile del trattino di sistema. |
| Dot | `5` | Stile punto quadrato. |
| Dash | `6` | Stile trattino. |
| LongDash | `7` | Stile trattino lungo. |
| DashDot | `8` | Trattino corto. |
| LongDashDot | `9` | Trattino lungo, trattino corto. |
| LongDashDotDot | `10` | Trattino lungo, trattino corto, trattino corto. |
| Default | `0` | Lo stesso diSolid . |

## Esempi

Mostra come creare forme diverse.

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

// 2 - Linea diagonale nera spessa con estremità arrotondate:
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

// 4 - Freccia con orientamento capovolto riempita con il logo Aspose:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Quando invertiamo l'orientamento della freccia, invertiamo anche l'immagine che la freccia contiene.
    // Capovolgi l'immagine nell'altro senso per annullare questo effetto prima di ottenere la forma per visualizzarlo.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Guarda anche

* property [DashStyle](../stroke/dashstyle/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
