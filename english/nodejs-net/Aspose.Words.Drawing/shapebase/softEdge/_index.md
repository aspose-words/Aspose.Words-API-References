---
title: ShapeBase.softEdge property
linktitle: softEdge property
articleTitle: softEdge property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.softEdge property. Gets soft edge formatting for the shape."
type: docs
weight: 490
url: /nodejs-net/aspose.words.drawing/shapebase/softEdge/
---

## ShapeBase.softEdge property

Gets soft edge formatting for the shape.


```js
get softEdge(): Aspose.Words.Drawing.SoftEdgeFormat
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
* class [ShapeBase](../)

