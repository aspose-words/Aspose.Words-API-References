﻿---
title: Shading.foregroundPatternColor property
linktitle: foregroundPatternColor property
articleTitle: foregroundPatternColor property
second_title: Aspose.Words for Node.js
description: "Shading.foregroundPatternColor property. Gets or sets the color that's applied to the foreground of the [Shading](../) object."
type: docs
weight: 40
url: /nodejs-net/aspose.words/shading/foregroundPatternColor/
---

## Shading.foregroundPatternColor property

Gets or sets the color that's applied to the foreground of the [Shading](../) object.



```js
get foregroundPatternColor(): string
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
* class [Shading](../)

