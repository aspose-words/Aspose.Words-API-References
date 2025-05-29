---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.GradientVariant für anpassbare Farbverlaufsfüllungen und verbessern Sie Ihre Dokumentdesigns mit lebendigen Stilen.
type: docs
weight: 1340
url: /de/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Gibt die Variante für eine Verlaufsfüllung an.

```csharp
public enum GradientVariant
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Farbverlaufsvariante „Keine“. |
| Variant1 | `1` | Farbverlaufsvariante 1. |
| Variant2 | `2` | Farbverlaufsvariante 2. |
| Variant3 | `3` | Farbverlaufsvariante 3. |
| Variant4 | `4` | Farbverlaufsvariante 4. |

## Bemerkungen

Entspricht den vier Varianten auf der Registerkarte „Farbverlauf“ im Dialogfeld „Fülleffekte“ in Word.

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
