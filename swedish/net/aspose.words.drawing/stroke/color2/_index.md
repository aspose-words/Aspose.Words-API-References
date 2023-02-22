---
title: Stroke.Color2
second_title: Aspose.Words för .NET API Referens
description: Stroke fast egendom. Definierar en andra färg för en linje.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Definierar en andra färg för en linje.

```csharp
public Color Color2 { get; set; }
```

### Anmärkningar

Standardvärdet för a[`Shape`](../../shape/) är White.

### Exempel

Visar hur man bearbetar formlinjefunktioner.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Strokes kan ha två färger, som används för att skapa ett mönster som definieras av tvåfärgade bilddata.
// Linjer med en enda färg använder inte egenskapen Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Se även

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../stroke/)
* hopsättning [Aspose.Words](../../../)


