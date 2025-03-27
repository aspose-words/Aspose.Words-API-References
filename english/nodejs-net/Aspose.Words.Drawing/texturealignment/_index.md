---
title: TextureAlignment enumeration
linktitle: TextureAlignment enumeration
articleTitle: TextureAlignment enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.TextureAlignment enumeration. Specifies the alignment for the tiling of the texture fill."
type: docs
weight: 510
url: /nodejs-net/Aspose.Words.Drawing/texturealignment/
---

## TextureAlignment enumeration

Specifies the alignment for the tiling of the texture fill.


### Members

| Name | Description |
| --- | --- |
| TopLeft | Top left texture alignment. |
| Top | Top texture alignment. |
| TopRight | Top right texture alignment. |
| Left | Left texture alignment. |
| Center | Center texture alignment. |
| Right | Right texture alignment. |
| BottomLeft | Bottom left texture alignment. |
| Bottom | Bottom texture alignment. |
| BottomRight | Bottom right texture alignment. |
| None | None texture alignment. |

### Examples

Shows how to fill and tiling the texture inside the shape.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 80, 80);

// Apply texture alignment to the shape fill.
shape.fill.presetTextured(aw.Drawing.PresetTexture.Canvas);
shape.fill.textureAlignment = aw.Drawing.TextureAlignment.TopRight;

// Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
// property after the document saves.
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Strict;

doc.save(base.artifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### See Also

* module [Aspose.Words.Drawing](../)

