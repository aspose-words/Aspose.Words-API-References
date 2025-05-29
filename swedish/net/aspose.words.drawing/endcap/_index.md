---
title: EndCap Enum
linktitle: EndCap
articleTitle: EndCap
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.EndCap-enum för anpassningsbara radkapslar. Förbättra dina dokumentdesigner med unika visuella effekter!
type: docs
weight: 1260
url: /sv/net/aspose.words.drawing/endcap/
---
## EndCap enumeration

Anger stilen för radövergången.

```csharp
public enum EndCap
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Round | `0` | Rundade ändar. |
| Square | `1` | Kvadraten sticker ut med halva linjebredden. |
| Flat | `2` | Linjen slutar vid slutpunkten. |
| Default | `2` | Standardvärdet ärFlat . |

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

* property [EndCap](../stroke/endcap/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
