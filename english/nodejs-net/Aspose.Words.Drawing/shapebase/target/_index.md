---
title: ShapeBase.target property
linktitle: target property
articleTitle: target property
second_title: Aspose.Words for Node.js
description: "ShapeBase.target property. Gets or sets the target frame for the shape hyperlink."
type: docs
weight: 560
url: /nodejs-net/aspose.words.drawing/shapebase/target/
---

## ShapeBase.target property

Gets or sets the target frame for the shape hyperlink.


```js
get target(): string
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

