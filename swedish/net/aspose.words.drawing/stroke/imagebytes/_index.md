---
title: Stroke.ImageBytes
second_title: Aspose.Words för .NET API Referens
description: Stroke fast egendom. Definierar bilden för en linjebild eller mönsterfyllning.
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Definierar bilden för en linjebild eller mönsterfyllning.

```csharp
public byte[] ImageBytes { get; }
```

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


