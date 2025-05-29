---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.GradientStop, Ihre Lösung zum Erstellen atemberaubender Farbverläufe mit anpassbaren Stopps für verbesserte Dokumentvisualisierungen.
type: docs
weight: 1310
url: /de/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Stellt einen Gradientenstopp dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit grafischen Elementen](https://docs.aspose.com/words/net/working-with-graphic-elements/) Dokumentationsartikel.

```csharp
public class GradientStop
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Initialisiert eine neue Instanz des`GradientStop` Klasse. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Initialisiert eine neue Instanz des`GradientStop` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Ruft einen Wert ab, der die Farbe des Farbverlaufsstopps ohne Modifikatoren darstellt. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der die Farbe des Farbverlaufsstopps darstellt. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der die Position eines Stopps innerhalb des Gradienten darstellt , ausgedrückt als Prozentsatz im Bereich von 0,0 bis 1,0. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der die Transparenz der Verlaufsfüllung darstellt, ausgedrückt als Prozentsatz im Bereich von 0,0 bis 1,0. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Entfernt den Gradientenstopp vom übergeordneten Element[`GradientStopCollection`](../gradientstopcollection/) . |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
