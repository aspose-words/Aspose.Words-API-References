---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.GradientStyle-enum för anpassningsbara gradientfyllningsstilar som förbättrar dina dokumentdesigner med livfulla bilder.
type: docs
weight: 1330
url: /sv/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

Anger stilen för en övertoningsfyllning.

```csharp
public enum GradientStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Ingen gradient. |
| Horizontal | `1` | Gradient som löper horisontellt över ett objekt. |
| Vertical | `2` | Gradient som löper vertikalt nerför ett objekt. |
| DiagonalUp | `3` | Diagonal gradient som rör sig från ett nedre hörn upp till det motsatta hörnet. |
| DiagonalDown | `4` | Diagonal gradient som rör sig från ett övre hörn ner till det motsatta hörnet. |
| FromCorner | `5` | Gradient som löper från ett hörn till de andra tre hörnen. |
| FromCenter | `6` | Gradient som löper från mitten ut till hörnen. |

## Exempel

Visar hur man fyller en form med övertoningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applicera enfärgad gradientfyllning på formen med ForeColor av gradientfyllningen.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Använd tvåfärgad gradientfyllning på formen.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Ändra bakfärg för gradientfyllning.
shape.Fill.BackColor = Color.Yellow;
// Observera att ändringarna i "GradientAngle" sker mot "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradientfyllning får ingen effekt, det fungerar bara för linjär gradient.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Använd alternativet compliance för att definiera formen med DML om du vill få "GradientStyle",
// Egenskaperna "GradientVariant" och "GradientAngle" efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
