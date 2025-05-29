---
title: Fill.GradientAngle
linktitle: GradientAngle
articleTitle: GradientAngle
second_title: Aspose.Words för .NET
description: Justera egenskapen GradientAngle för att anpassa din gradientfyllnings vinkel, vilket enkelt förbättrar din designs djup och visuella attraktionskraft.
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/fill/gradientangle/
---
## Fill.GradientAngle property

Hämtar eller ställer in vinkeln på gradientfyllningen.

```csharp
public double GradientAngle { get; set; }
```

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

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
