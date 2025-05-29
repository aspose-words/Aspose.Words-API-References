---
title: GradientStopCollection Class
linktitle: GradientStopCollection
articleTitle: GradientStopCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.GradientStopCollection, die eine robuste Sammlung anpassbarer GradientStop-Objekte für ein verbessertes Dokumentdesign bietet.
type: docs
weight: 1320
url: /de/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

Enthält eine Sammlung von[`GradientStop`](../gradientstop/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit grafischen Elementen](https://docs.aspose.com/words/net/working-with-graphic-elements/) Dokumentationsartikel.

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | Ruft einen ganzzahligen Wert ab, der die Anzahl der Elemente in der Sammlung angibt. |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | Ruft ab oder setzt einen[`GradientStop`](../gradientstop/) Objekt in der Sammlung. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(*[GradientStop](../gradientstop/)*) | Fügt einen angegebenen[`GradientStop`](../gradientstop/) zu einem Farbverlauf. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | Gibt einen Enumerator zurück, der die Sammlung durchläuft. |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(*int, [GradientStop](../gradientstop/)*) | Fügt ein[`GradientStop`](../gradientstop/) zur Sammlung an einem angegebenen Index. |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(*[GradientStop](../gradientstop/)*) | Entfernt eine angegebene[`GradientStop`](../gradientstop/) aus der Sammlung. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(*int*) | Entfernt ein[`GradientStop`](../gradientstop/) aus der Sammlung an einem angegebenen Index. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`GradientStops`](../fill/gradientstops/) Eigenschaft für den Zugriff auf Farbverlaufsstopps von Füllobjekten.

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

* class [GradientStop](../gradientstop/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
