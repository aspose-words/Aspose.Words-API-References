---
title: GradientStopCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: GradientStopCollection Remove methode. Entfernt eine angegebeneGradientStop aus der Sammlung in C#.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/gradientstopcollection/remove/
---
## GradientStopCollection.Remove method

Entfernt eine angegebene[`GradientStop`](../../gradientstop/) aus der Sammlung.

```csharp
public bool Remove(GradientStop gradientStop)
```

### Rückgabewert

`WAHR` wenn der Gradientenstopp erfolgreich entfernt wurde, andernfalls`FALSCH`.

## Beispiele

Zeigt, wie man der Verlaufsfüllung Verlaufsstopps hinzufügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Gradient-Stopp-Sammlung abrufen.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Ersten Gradientenstopp ändern.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Neuen Verlaufsstopp am Ende der Sammlung hinzufügen.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Gradientenstopp bei Index 1 entfernen.
gradientStops.RemoveAt(1);
// Und neuen Gradientenstopp am gleichen Index 1 einfügen.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Letzten Farbverlaufsstopp in der Sammlung entfernen.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Verwenden Sie die Compliance-Option, um die Form mithilfe von DML zu definieren
// wenn Sie die Eigenschaft „GradientStops“ erhalten möchten, nachdem das Dokument gespeichert wurde.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Siehe auch

* class [GradientStop](../../gradientstop/)
* class [GradientStopCollection](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
