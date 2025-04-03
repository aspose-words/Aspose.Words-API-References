---
title: Font.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for NodeJs
description: "Font.shading property. Returns a [Shading](../../shading/) object that refers to the shading formatting for the font."
type: docs
weight: 330
url: /nodejs-net/aspose.words/font/shading/
---

## Font.shading property

Returns a [Shading](../../shading/) object that refers to the shading formatting for the font.



```js
get shading(): Aspose.Words.Shading
```

### Examples

Shows how to apply shading to text created by a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.color = "#FFFFFF";

// One way to make the text created using our white font color visible
// is to apply a background shading effect.
let shading = builder.font.shading;
shading.texture = aw.TextureIndex.TextureDiagonalUp;
shading.backgroundPatternColor = "#FF4500";
shading.foregroundPatternColor = "#00008B";

builder.writeln("White text on an orange background with a two-tone texture.");

doc.save(base.artifactsDir + "Font.shading.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

