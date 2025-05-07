---
title: SoftEdgeFormat.radius property
linktitle: radius property
articleTitle: radius property
second_title: Aspose.Words for Node.js
description: "SoftEdgeFormat.radius property. Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt)"
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing/softedgeformat/radius/
---

## SoftEdgeFormat.radius property

Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt).
The default value is 0.0.


```js
get radius(): number
```

### Examples

Shows how to set limit for image resolution.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.SvgSaveOptions();
saveOptions.maxImageResolution = 72;

doc.save(base.artifactsDir + "SvgSaveOptions.maxImageResolution.svg", saveOptions);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [SoftEdgeFormat](../)

