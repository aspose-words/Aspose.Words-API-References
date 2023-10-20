---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words für .NET
description: Fill OneColorGradient methode. Setzt die angegebene Füllung auf einen einfarbigen Farbverlauf in C#.
type: docs
weight: 210
url: /de/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

Setzt die angegebene Füllung auf einen einfarbigen Farbverlauf.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | GradientStyle | Der Verlaufsstil[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | Die Verlaufsvariante[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Der Grad der Steigung. Kann ein Wert zwischen 0,0 (dunkel) und 1,0 (hell) sein. |

## Beispiele

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
// Zweifarbige Farbverlaufsfüllung auf die Form anwenden.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// BackColor der Farbverlaufsfüllung ändern.
shape.Fill.BackColor = Color.Yellow;
// Beachten Sie, dass sich „GradientAngle“ für „GradientStyle.FromCorner/GradientStyle.FromCenter“ ändert.
// Farbverlaufsfüllungen haben keinen Effekt, sie funktionieren nur bei linearen Farbverläufen.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Verwenden Sie die Compliance-Option, um die Form mithilfe von DML zu definieren, wenn Sie „GradientStyle“ erhalten möchten.
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

Setzt die angegebene Füllung auf einen einfarbigen Farbverlauf unter Verwendung der angegebenen Farbe.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| color | Color | Die Farbe zum Erstellen des Farbverlaufs. |
| style | GradientStyle | Der Verlaufsstil[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | Die Verlaufsvariante[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Der Grad der Steigung. Kann ein Wert zwischen 0,0 (dunkel) und 1,0 (hell) sein. |

## Beispiele

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
// Zweifarbige Farbverlaufsfüllung auf die Form anwenden.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// BackColor der Farbverlaufsfüllung ändern.
shape.Fill.BackColor = Color.Yellow;
// Beachten Sie, dass sich „GradientAngle“ für „GradientStyle.FromCorner/GradientStyle.FromCenter“ ändert.
// Farbverlaufsfüllungen haben keinen Effekt, sie funktionieren nur bei linearen Farbverläufen.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Verwenden Sie die Compliance-Option, um die Form mithilfe von DML zu definieren, wenn Sie „GradientStyle“ erhalten möchten.
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
