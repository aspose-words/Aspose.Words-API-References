---
title: Enum GradientStyle
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.GradientStyle opsomming. Gibt den Stil für eine Verlaufsfüllung an.
type: docs
weight: 1000
url: /de/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

Gibt den Stil für eine Verlaufsfüllung an.

```csharp
public enum GradientStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `-1` | Kein Farbverlauf. |
| Horizontal | `1` | Farbverlauf, der horizontal über ein Objekt verläuft. |
| Vertical | `2` | Farbverlauf, der vertikal an einem Objekt herunterläuft. |
| DiagonalUp | `3` | Diagonaler Farbverlauf, der sich von einer unteren Ecke nach oben zur gegenüberliegenden Ecke bewegt. |
| DiagonalDown | `4` | Diagonaler Farbverlauf, der sich von einer oberen Ecke nach unten zur gegenüberliegenden Ecke bewegt. |
| FromCorner | `5` | Farbverlauf, der von einer Ecke zu den anderen drei Ecken verläuft. |
| FromCenter | `6` | Farbverlauf, der von der Mitte zu den Ecken verläuft. |

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


