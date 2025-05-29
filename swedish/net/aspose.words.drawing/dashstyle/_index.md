---
title: DashStyle Enum
linktitle: DashStyle
articleTitle: DashStyle
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.DashStyle-enum för mångsidiga streckade linjestilar. Förbättra dina dokumentdesigner med anpassningsbara visuella element.
type: docs
weight: 1250
url: /sv/net/aspose.words.drawing/dashstyle/
---
## DashStyle enumeration

Streckad linjestil.

```csharp
public enum DashStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Solid | `0` | Heldragen (kontinuerlig) penna. |
| ShortDash | `1` | Systemets instrumentpanelsstil. |
| ShortDot | `2` | Systemets instrumentpanelsstil. |
| ShortDashDot | `3` | Systemets instrumentpanelsstil. |
| ShortDashDotDot | `4` | Systemets instrumentpanelsstil. |
| Dot | `5` | Fyrkantig prickstil. |
| Dash | `6` | Dash-stil. |
| LongDash | `7` | Lång streckstil. |
| DashDot | `8` | Streck kort streck. |
| LongDashDot | `9` | Långt streck kort streck. |
| LongDashDotDot | `10` | Långt streck kort streck kort streck. |
| Default | `0` | Samma somSolid . |

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

* property [DashStyle](../stroke/dashstyle/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
