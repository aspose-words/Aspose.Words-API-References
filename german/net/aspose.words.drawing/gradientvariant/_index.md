---
title: Enum GradientVariant
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.GradientVariant opsomming. Gibt die Variante für eine Verlaufsfüllung an.
type: docs
weight: 1010
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
| None | `0` | Verlaufsvariante „Keine“. |
| Variant1 | `1` | Verlaufsvariante 1. |
| Variant2 | `2` | Verlaufsvariante 2. |
| Variant3 | `3` | Verlaufsvariante 3. |
| Variant4 | `4` | Verlaufsvariante 4. |

### Bemerkungen

Entspricht den vier Varianten auf der Registerkarte „Verlauf“ im Dialogfeld „Fülleffekte“ in Word.

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


