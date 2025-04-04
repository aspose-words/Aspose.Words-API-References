---
title: ShapeBase.alternativeText property
linktitle: alternativeText property
articleTitle: alternativeText property
second_title: Aspose.Words for Node.js
description: "ShapeBase.alternativeText property. Defines alternative text to be displayed instead of a graphic."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing/shapebase/alternativeText/
---

## ShapeBase.alternativeText property

Defines alternative text to be displayed instead of a graphic.


```js
get alternativeText(): string
```

### Remarks

The default value is an empty string.




### Examples

Shows how to use a shape's alternative text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let shape = builder.insertShape(aw.Drawing.ShapeType.Cube, 150, 150);
shape.name = "MyCube";

shape.alternativeText = "Alt text for MyCube.";

// We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
doc.save(base.artifactsDir + "Shape.AltText.docx");

// Save the document to HTML, and then delete the linked image that belongs to our shape.
// The browser that is reading our HTML will display the alt text in place of the missing image.
doc.save(base.artifactsDir + "Shape.AltText.html");
expect(fs.existsSync(base.artifactsDir + "Shape.AltText.001.png")).toEqual(true);
fs.rmSync(base.artifactsDir + "Shape.AltText.001.png");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

