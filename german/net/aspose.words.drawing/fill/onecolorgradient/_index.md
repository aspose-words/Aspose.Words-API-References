---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der OneColorGradient-Methode beeindruckende einfarbige Farbverläufe für Ihre Designs erstellen. Optimieren Sie Ihre Projekte mühelos!
type: docs
weight: 220
url: /de/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

Legt die angegebene Füllung auf einen einfarbigen Farbverlauf fest.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | GradientStyle | Der Farbverlaufsstil[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | Die Gradientenvariante[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Der Grad des Farbverlaufs. Kann ein Wert zwischen 0,0 (dunkel) und 1,0 (hell) sein. |

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

## OneColorGradient(*Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient_1}

Legt die angegebene Füllung auf einen einfarbigen Farbverlauf mit der angegebenen Farbe fest.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| color | Color | Die Farbe zum Erstellen des Farbverlaufs. |
| style | GradientStyle | Der Farbverlaufsstil[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | Die Gradientenvariante[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Der Grad des Farbverlaufs. Kann ein Wert zwischen 0,0 (dunkel) und 1,0 (hell) sein. |

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
