---
title: TwoColorGradient
second_title: Aspose.Words för .NET API Referens
description: Ställer in den angivna fyllningen till en tvåfärgsgradient.
type: docs
weight: 210
url: /sv/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(GradientStyle, GradientVariant) {#twocolorgradient}

Ställer in den angivna fyllningen till en tvåfärgsgradient.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| style | GradientStyle | Gradientstilen[`GradientStyle`](../../gradientstyle). |
| variant | GradientVariant | Gradientvarianten[`GradientVariant`](../../gradientvariant) |

### Exempel

Visar hur man fyller en form med övertoningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applicera enfärgad övertoningsfyllning på formen med ForeColor av övertoningsfyllning.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applicera tvåfärgsgradientfyllning på formen.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Ändra BackColor för gradientfyllning.
shape.Fill.BackColor = Color.Yellow;
// Observera att "GradientAngle" ändras för "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradientfyllning får ingen effekt, det fungerar bara för linjär gradient.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "GradientStyle",
// Egenskaperna "GradientVariant" och "GradientAngle" efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Se även

* enum [GradientStyle](../../gradientstyle)
* enum [GradientVariant](../../gradientvariant)
* class [Fill](../../fill)
* namnutrymme [Aspose.Words.Drawing](../../fill)
* hopsättning [Aspose.Words](../../../)

---

## TwoColorGradient(Color, Color, GradientStyle, GradientVariant) {#twocolorgradient_1}

Ställer in den angivna fyllningen till en tvåfärgsgradient.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| color1 | Color | Den första färgen för att bygga övertoningen. |
| color2 | Color | Den andra färgen för att bygga gradienten. |
| style | GradientStyle | Gradientstilen[`GradientStyle`](../../gradientstyle). |
| variant | GradientVariant | Gradientvarianten[`GradientVariant`](../../gradientvariant) |

### Exempel

Visar hur man fyller en form med övertoningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applicera enfärgad övertoningsfyllning på formen med ForeColor av övertoningsfyllning.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applicera tvåfärgsgradientfyllning på formen.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Ändra BackColor för gradientfyllning.
shape.Fill.BackColor = Color.Yellow;
// Observera att "GradientAngle" ändras för "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradientfyllning får ingen effekt, det fungerar bara för linjär gradient.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "GradientStyle",
// Egenskaperna "GradientVariant" och "GradientAngle" efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Se även

* enum [GradientStyle](../../gradientstyle)
* enum [GradientVariant](../../gradientvariant)
* class [Fill](../../fill)
* namnutrymme [Aspose.Words.Drawing](../../fill)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
