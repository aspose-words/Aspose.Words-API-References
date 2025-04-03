---
title: ShapeBase.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.title property. Gets or sets the title (caption) of the current shape object."
type: docs
weight: 510
url: /nodejs-net/Aspose.Words.Drawing/shapebase/title/
---

## ShapeBase.title property

Gets or sets the title (caption) of the current shape object.


```js
get title(): string
```

### Remarks

Default is empty string.

Cannot be ``null``, but can be an empty string.




### Examples

Shows how to set the title of a shape.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a shape, give it a title, and then add it to the document.
let shape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Cube);
shape.width = 200;
shape.height = 200;
shape.title = "My cube";

builder.insertNode(shape);

// When we save a document with a shape that has a title,
// Aspose.words will store that title in the shape's Alt Text.
doc.save(base.artifactsDir + "Shape.title.docx");

doc = new aw.Document(base.artifactsDir + "Shape.title.docx");
shape = doc.getShape(0, true);

expect(shape.title).toEqual('');
expect(shape.alternativeText).toEqual("Title: My cube");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

