---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words for .NET
description: Fill TextureAlignment property. Gets or sets the alignment for tile texture fill in C#.
type: docs
weight: 190
url: /net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Gets or sets the alignment for tile texture fill.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## Examples

Shows how to fill and tiling the texture inside the shape.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Apply texture alignment to the shape fill.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
// property after the document saves.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### See Also

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
