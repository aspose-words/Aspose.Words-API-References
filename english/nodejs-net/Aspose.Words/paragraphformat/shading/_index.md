---
title: ParagraphFormat.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.shading property. Returns a [Shading](../../shading/) object that refers to the shading formatting for the paragraph."
type: docs
weight: 290
url: /nodejs-net/aspose.words/paragraphformat/shading/
---

## ParagraphFormat.shading property

Returns a [Shading](../../shading/) object that refers to the shading formatting for the paragraph.



```js
get shading(): Aspose.Words.Shading
```

### Examples

Shows how to decorate text with borders and shading.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let borders = builder.paragraphFormat.borders;
borders.distanceFromText = 20;
borders.at(aw.BorderType.Left).lineStyle = aw.LineStyle.Double;
borders.at(aw.BorderType.Right).lineStyle = aw.LineStyle.Double;
borders.at(aw.BorderType.Top).lineStyle = aw.LineStyle.Double;
borders.at(aw.BorderType.Bottom).lineStyle = aw.LineStyle.Double;

let shading = builder.paragraphFormat.shading;
shading.texture = aw.TextureIndex.TextureDiagonalCross;
shading.backgroundPatternColor = "#F08080";
shading.foregroundPatternColor = "#FFA07A";

builder.write("This paragraph is formatted with a double border and shading.");
doc.save(base.artifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

