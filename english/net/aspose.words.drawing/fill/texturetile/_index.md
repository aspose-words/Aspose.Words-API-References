---
title: Fill.TextureTile
linktitle: TextureTile
articleTitle: TextureTile
second_title: Aspose.Words for .NET
description: Fill TextureTile property. Returns True if the current fill is a tile texture fill.
type: docs
weight: 210
url: /net/aspose.words.drawing/fill/texturetile/
---
## Fill.TextureTile property

Returns True if the current fill is a tile texture fill.

```csharp
public bool TextureTile { get; }
```

## Examples

Shows how to scale a tiled texture fill of a shape.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);
shape.Fill.PresetTextured(PresetTexture.Canvas);

Fill fill = shape.Fill;

// Check whether the shape's fill is a tiled texture before scaling it.
if (fill.TextureTile)
{
    // A scale of 1 is equivalent to 100%. Values can exceed 100%.
    fill.TextureHorizontalScale = 0.5;
    fill.TextureVerticalScale = 2.15;
}

// Use the compliance option to define the shape using DML
// to keep the texture scale properties after the document saves.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };
doc.Save(ArtifactsDir + "Shape.TextureTile.docx", saveOptions);
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
