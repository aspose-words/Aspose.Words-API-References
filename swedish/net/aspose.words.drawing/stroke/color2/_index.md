---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Stroke Color2 – förbättra dina designer med en anpassningsbar andra streckfärg för livfulla och iögonfallande bilder.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Definierar en andra färg för ett streck.

```csharp
public Color Color2 { get; set; }
```

## Anmärkningar

Standardvärdet för en[`Shape`](../../shape/) är White .

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
