---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.GlowFormat, um Ihre Dokumente mit atemberaubenden Leuchteffekten zu verschönern. Werten Sie Ihr Design mit einzigartigen Formatierungsoptionen auf!
type: docs
weight: 1300
url: /de/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Stellt die Leuchtformatierung für ein Objekt dar.

```csharp
public class GlowFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Ruft ab oder setzt einenColor Objekt, das die Farbe für einen Leuchteffekt darstellt. Der Standardwert istBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der die Länge des Radius für einen Leuchteffekt in Punkten (pt) darstellt. Der Standardwert ist 0,0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Ruft den Transparenzgrad für den Leuchteffekt als Wert zwischen 0,0 (undurchsichtig) und 1,0 (transparent) ab oder legt ihn fest. Der Standardwert ist 0,0. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Entfernt`GlowFormat` vom übergeordneten Objekt. |

## Bemerkungen

Verwenden Sie die[`Glow`](../shapebase/glow/) Eigenschaft, um auf die Leuchteigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der`GlowFormat` Klasse direkt.

## Beispiele

Zeigt, wie mit dem Leuchtformeffekt interagiert wird.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
