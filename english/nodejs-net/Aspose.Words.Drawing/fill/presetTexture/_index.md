---
title: Fill.presetTexture property
linktitle: presetTexture property
articleTitle: presetTexture property
second_title: Aspose.Words for Node.js
description: "Fill.presetTexture property. Gets a [PresetTexture](../../presettexture/) for the fill."
type: docs
weight: 170
url: /nodejs-net/aspose.words.drawing/fill/presetTexture/
---

## Fill.presetTexture property

Gets a [PresetTexture](../../presettexture/) for the fill.



```js
get presetTexture(): Aspose.Words.Drawing.PresetTexture
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

doc = new aw.Document(base.artifactsDir + "Shape.TextureFill.docx");

shape = doc.getShape(0, true);

expect(shape.fill.textureAlignment).toEqual(aw.Drawing.TextureAlignment.TopRight);
expect(shape.fill.presetTexture).toEqual(aw.Drawing.PresetTexture.Canvas);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

