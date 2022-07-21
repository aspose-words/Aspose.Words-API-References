---
title: TwoColorGradient
second_title: Aspose.Words für .NET-API-Referenz
description: Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest.
type: docs
weight: 210
url: /de/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(GradientStyle, GradientVariant) {#twocolorgradient}

Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | GradientStyle | Der Verlaufsstil[`GradientStyle`](../../gradientstyle). |
| variant | GradientVariant | Die Verlaufsvariante[`GradientVariant`](../../gradientvariant) |

### Beispiele

Zeigt, wie eine Form mit Farbverläufen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Anwenden einer einfarbigen Verlaufsfüllung auf die Form mit ForeColor der Verlaufsfüllung.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Zweifarbige Verlaufsfüllung auf die Form anwenden.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// BackColor der Farbverlaufsfüllung ändern.
shape.Fill.BackColor = Color.Yellow;
// Beachten Sie, dass "GradientAngle" für "GradientStyle.FromCorner/GradientStyle.FromCenter" geändert wird
// Verlaufsfüllung bekommt keinen Effekt, es funktioniert nur für linearen Verlauf.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie "GradientStyle" erhalten möchten.
// Eigenschaften "GradientVariant" und "GradientAngle" nach dem Speichern des Dokuments.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Siehe auch

* enum [GradientStyle](../../gradientstyle)
* enum [GradientVariant](../../gradientvariant)
* class [Fill](../../fill)
* namensraum [Aspose.Words.Drawing](../../fill)
* Montage [Aspose.Words](../../../)

---

## TwoColorGradient(Color, Color, GradientStyle, GradientVariant) {#twocolorgradient_1}

Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| color1 | Color | Die erste Farbe, die den Farbverlauf bildet. |
| color2 | Color | Die zweite Farbe zum Erstellen des Farbverlaufs. |
| style | GradientStyle | Der Verlaufsstil[`GradientStyle`](../../gradientstyle). |
| variant | GradientVariant | Die Verlaufsvariante[`GradientVariant`](../../gradientvariant) |

### Beispiele

Zeigt, wie eine Form mit Farbverläufen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Anwenden einer einfarbigen Verlaufsfüllung auf die Form mit ForeColor der Verlaufsfüllung.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Zweifarbige Verlaufsfüllung auf die Form anwenden.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// BackColor der Farbverlaufsfüllung ändern.
shape.Fill.BackColor = Color.Yellow;
// Beachten Sie, dass "GradientAngle" für "GradientStyle.FromCorner/GradientStyle.FromCenter" geändert wird
// Verlaufsfüllung bekommt keinen Effekt, es funktioniert nur für linearen Verlauf.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie "GradientStyle" erhalten möchten.
// Eigenschaften "GradientVariant" und "GradientAngle" nach dem Speichern des Dokuments.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Siehe auch

* enum [GradientStyle](../../gradientstyle)
* enum [GradientVariant](../../gradientvariant)
* class [Fill](../../fill)
* namensraum [Aspose.Words.Drawing](../../fill)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
