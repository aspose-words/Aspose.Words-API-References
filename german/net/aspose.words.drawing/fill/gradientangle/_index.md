---
title: Fill.GradientAngle
second_title: Aspose.Words für .NET-API-Referenz
description: Fill eigendom. Ruft den Winkel der Verlaufsfüllung ab oder legt ihn fest.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/fill/gradientangle/
---
## Fill.GradientAngle property

Ruft den Winkel der Verlaufsfüllung ab oder legt ihn fest.

```csharp
public double GradientAngle { get; set; }
```

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

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../fill/)
* Montage [Aspose.Words](../../../)


