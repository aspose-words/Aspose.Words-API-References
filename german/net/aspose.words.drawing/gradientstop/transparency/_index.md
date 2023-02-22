---
title: GradientStop.Transparency
second_title: Aspose.Words für .NET-API-Referenz
description: GradientStop eigendom. Ruft einen Wert ab oder legt einen Wert fest der die Transparenz der Farbverlaufsfüllung darstellt ausgedrückt als Prozent im Bereich von 00 bis 10.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/gradientstop/transparency/
---
## GradientStop.Transparency property

Ruft einen Wert ab oder legt einen Wert fest, der die Transparenz der Farbverlaufsfüllung darstellt, ausgedrückt als Prozent im Bereich von 0,0 bis 1,0.

```csharp
public double Transparency { get; set; }
```

### Beispiele

Zeigt, wie Sie Verlaufsstopps zur Verlaufsfüllung hinzufügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Sammlung von Farbverlaufsstopps abrufen.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Ersten Gradientenstopp ändern.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Neuen Gradientenstopp am Ende der Sammlung hinzufügen.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Entfernen Sie den Gradientenstopp bei Index 1.
gradientStops.RemoveAt(1);
// Und neuen Gradientenstopp am selben Index 1 einfügen.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Letzten Gradientenstopp in der Sammlung entfernen.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren
// Wenn Sie die Eigenschaft "GradientStops" erhalten möchten, nachdem das Dokument gespeichert wurde.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Siehe auch

* class [GradientStop](../)
* namensraum [Aspose.Words.Drawing](../../gradientstop/)
* Montage [Aspose.Words](../../../)


