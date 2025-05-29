---
title: Fill.TwoColorGradient
linktitle: TwoColorGradient
articleTitle: TwoColorGradient
second_title: Aspose.Words für .NET
description: Wenden Sie mit unserer Methode „Zweifarbigen Farbverlauf füllen“ eine beeindruckende zweifarbige Farbverlaufsfüllung an und werten Sie Ihre Designs mit lebendigen, anpassbaren Effekten auf.
type: docs
weight: 270
url: /de/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/)*) {#twocolorgradient}

Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | GradientStyle | Der Farbverlaufsstil[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | Die Gradientenvariante[`GradientVariant`](../../gradientvariant/) |

## Beispiele

Zeigt, wie eine Form mit Farbverläufen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Wenden Sie eine einfarbige Verlaufsfüllung auf die Form mit der Vorderfarbe der Verlaufsfüllung an.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Zweifarbige Verlaufsfüllung auf die Form anwenden.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Hintergrundfarbe der Verlaufsfüllung ändern.
shape.Fill.BackColor = Color.Yellow;
// Beachten Sie, dass sich „GradientAngle“ für „GradientStyle.FromCorner/GradientStyle.FromCenter“ ändert.
// Die Farbverlaufsfüllung hat keinen Effekt, sie funktioniert nur bei linearen Farbverläufen.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie „GradientStyle“ erhalten möchten.
// Eigenschaften „GradientVariant“ und „GradientAngle“, nachdem das Dokument gespeichert wurde.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Siehe auch

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)

---

## TwoColorGradient(*Color, Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/)*) {#twocolorgradient_1}

Legt die angegebene Füllung auf einen zweifarbigen Farbverlauf fest.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| color1 | Color | Die erste Farbe zum Erstellen des Farbverlaufs. |
| color2 | Color | Die zweite Farbe zum Erstellen des Farbverlaufs. |
| style | GradientStyle | Der Farbverlaufsstil[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | Die Gradientenvariante[`GradientVariant`](../../gradientvariant/) |

## Beispiele

Zeigt, wie eine Form mit Farbverläufen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Wenden Sie eine einfarbige Verlaufsfüllung auf die Form mit der Vorderfarbe der Verlaufsfüllung an.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Zweifarbige Verlaufsfüllung auf die Form anwenden.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Hintergrundfarbe der Verlaufsfüllung ändern.
shape.Fill.BackColor = Color.Yellow;
// Beachten Sie, dass sich „GradientAngle“ für „GradientStyle.FromCorner/GradientStyle.FromCenter“ ändert.
// Die Farbverlaufsfüllung hat keinen Effekt, sie funktioniert nur bei linearen Farbverläufen.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren, wenn Sie „GradientStyle“ erhalten möchten.
// Eigenschaften „GradientVariant“ und „GradientAngle“, nachdem das Dokument gespeichert wurde.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Siehe auch

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
