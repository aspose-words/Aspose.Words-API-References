---
title: ShapeBase.screenTip property
linktitle: screenTip property
articleTitle: screenTip property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.screenTip property. Defines the text displayed when the mouse pointer moves over the shape."
type: docs
weight: 460
url: /nodejs-net/Aspose.Words.Drawing/shapebase/screenTip/
---

## ShapeBase.screenTip property

Defines the text displayed when the mouse pointer moves over the shape.


```js
get screenTip(): string
```

### Remarks

The default value is an empty string.




### Examples

Shows how to insert a shape which contains an image, and is also a hyperlink.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.href = "https://forum.aspose.com/";
shape.target = "New Window";
shape.screenTip = "Aspose.words Support Forums";

// Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
// and take us to the hyperlink in the "HRef" property.
doc.save(base.artifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

