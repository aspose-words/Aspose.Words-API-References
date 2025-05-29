---
title: Fill.GradientStyle
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words för .NET
description: Upptäck hur du kan förbättra dina designer med egenskapen GradientStyle för fantastiska fyllningseffekter. Förhöj dina projekt med livfulla gradienter!
type: docs
weight: 120
url: /sv/net/aspose.words.drawing/fill/gradientstyle/
---
## Fill.GradientStyle property

Hämtar gradientstilen[`GradientStyle`](../../gradientstyle/) för fyllningen.

```csharp
public GradientStyle GradientStyle { get; }
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

* enum [GradientStyle](../../gradientstyle/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
