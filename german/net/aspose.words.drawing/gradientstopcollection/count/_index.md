---
title: GradientStopCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „GradientStopCollection Count“, die die Gesamtzahl der Elemente angibt und so die Effizienz Ihrer Datenverwaltung und UI-Gestaltung verbessert.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/gradientstopcollection/count/
---
## GradientStopCollection.Count property

Ruft einen ganzzahligen Wert ab, der die Anzahl der Elemente in der Sammlung angibt.

```csharp
public int Count { get; }
```

## Beispiele

Zeigt, wie der Verlaufsfüllung Verlaufsstopps hinzugefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Sammlung von Gradientenstopps abrufen.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Ersten Gradientenstopp ändern.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Neuen Farbverlaufsstopp am Ende der Sammlung hinzufügen.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Gradientenstopp bei Index 1 entfernen.
gradientStops.RemoveAt(1);
// Und neuen Gradientenstopp am gleichen Index 1 einfügen.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Letzten Gradientenstopp in der Sammlung entfernen.
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

// Verwenden Sie die Compliance-Option, um die Form mit DML zu definieren
// wenn Sie die Eigenschaft „GradientStops“ erhalten möchten, nachdem das Dokument gespeichert wurde.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Siehe auch

* class [GradientStopCollection](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
