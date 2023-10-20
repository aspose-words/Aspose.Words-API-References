---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words für .NET
description: Stroke Color2 eigendom. Definiert eine zweite Farbe für einen Strich in C#.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Definiert eine zweite Farbe für einen Strich.

```csharp
public Color Color2 { get; set; }
```

## Bemerkungen

Der Standardwert für a[`Shape`](../../shape/) is White.

## Beispiele

Zeigt, wie Formstrich-Features verarbeitet werden.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Striche können zwei Farben haben, die zum Erstellen eines durch zweifarbige Bilddaten definierten Musters verwendet werden.
// Striche mit einer einzelnen Farbe verwenden nicht die Color2-Eigenschaft.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Siehe auch

* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
