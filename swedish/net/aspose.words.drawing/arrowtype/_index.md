---
title: ArrowType Enum
linktitle: ArrowType
articleTitle: ArrowType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.ArrowType-enum för att anpassa pilstilar för radslut, vilket förbättrar dokumentets visuella attraktionskraft och precision.
type: docs
weight: 730
url: /sv/net/aspose.words.drawing/arrowtype/
---
## ArrowType enumeration

Anger typen av pil i slutet av en linje.

```csharp
public enum ArrowType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Linjen har ingen pil i slutet. |
| Arrow | `1` | Pilen är en heldragen triangel. |
| Stealth | `2` | Pilen är en "smygande" pil. |
| Diamond | `3` | Linjeänden är en solid diamant. |
| Oval | `4` | Linjens slut är en heldragen oval. |
| Open | `5` | Pilen är en öppen pil. |
| Default | `0` | Samma somNone . |

## Exempel

Visar hur man skapar en mängd olika former.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer fyra exempel på former som vi kan infoga i våra dokument.
// 1 - Prickad, horisontell, halvtransparent röd linje
// med en pil i vänster ände och en diamant i höger ände:
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

// 2 - Tjock svart diagonal linje med rundade ändar:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Pil med grön fyllning:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Pil med en omvänd orientering fylld med Aspose-logotypen:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // När vi vänder orienteringen på vår pil, vänder vi också bilden som pilen innehåller.
    // Vänd bilden åt andra hållet för att ta bort detta innan du får formen för att visa den.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Se även

* property [StartArrowType](../stroke/startarrowtype/)
* property [EndArrowType](../stroke/endarrowtype/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
