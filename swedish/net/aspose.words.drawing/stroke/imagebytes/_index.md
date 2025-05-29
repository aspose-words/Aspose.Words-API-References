---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words för .NET
description: Upptäck hur du använder ImageBytes-egenskapen för att skapa fantastiska penseldrag och unika mönsterfyllningar för dina designer. Förbättra dina bilder idag!
type: docs
weight: 160
url: /sv/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Definierar bilden för en linjebild eller mönsterfyllning.

```csharp
public byte[] ImageBytes { get; }
```

## Exempel

Visar hur man bearbetar former och penseldrag.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Linjer kan ha två färger, vilka används för att skapa ett mönster som definieras av tvåtonsbilddata.
// Linjer med en enda färg använder inte egenskapen Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Se även

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
