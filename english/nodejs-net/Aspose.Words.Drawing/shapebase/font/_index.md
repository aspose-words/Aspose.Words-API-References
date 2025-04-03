---
title: ShapeBase.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.font property. Provides access to the font formatting of this object."
type: docs
weight: 140
url: /nodejs-net/aspose.words.drawing/shapebase/font/
---

## ShapeBase.font property

Provides access to the font formatting of this object.


```js
get font(): Aspose.Words.Font
```

### Examples

Shows how to insert a text box, and set the font of its contents.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

let shape = builder.insertShape(aw.Drawing.ShapeType.TextBox, 300, 50);
builder.moveTo(shape.lastParagraph);
builder.write("This text is inside the text box.");

// Set the "Hidden" property of the shape's "Font" object to "true" to hide the text box from sight
// and collapse the space that it would normally occupy.
// Set the "Hidden" property of the shape's "Font" object to "false" to leave the text box visible.
shape.font.hidden = hideShape;

// If the shape is visible, we will modify its appearance via the font object.
if (!hideShape)
{
  shape.font.highlightColor = "#D3D3D3";
  shape.font.color = "#FF0000";
  shape.font.underline = aw.Underline.Dash;
}

// Move the builder out of the text box back into the main document.
builder.moveTo(shape.parentParagraph);

builder.writeln("\nThis text is outside the text box.");

doc.save(base.artifactsDir + "Shape.font.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

