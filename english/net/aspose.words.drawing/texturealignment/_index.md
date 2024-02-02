---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.TextureAlignment enum. Specifies the alignment for the tiling of the texture fill in C#.
type: docs
weight: 1490
url: /net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Specifies the alignment for the tiling of the texture fill.

```csharp
public enum TextureAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| TopLeft | `0` | Top left texture alignment. |
| Top | `1` | Top texture alignment. |
| TopRight | `2` | Top right texture alignment. |
| Left | `3` | Left texture alignment. |
| Center | `4` | Center texture alignment. |
| Right | `5` | Right texture alignment. |
| BottomLeft | `6` | Bottom left texture alignment. |
| Bottom | `7` | Bottom texture alignment. |
| BottomRight | `8` | Bottom right texture alignment. |
| None | `9` | None texture alignment. |

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
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
