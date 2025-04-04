---
title: Fill.textureAlignment property
linktitle: textureAlignment property
articleTitle: textureAlignment property
second_title: Aspose.Words for Node.js
description: "Fill.textureAlignment property. Gets or sets the alignment for tile texture fill."
type: docs
weight: 190
url: /nodejs-net/aspose.words.drawing/fill/textureAlignment/
---

## Fill.textureAlignment property

Gets or sets the alignment for tile texture fill.


```js
get textureAlignment(): Aspose.Words.Drawing.TextureAlignment
```

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

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

