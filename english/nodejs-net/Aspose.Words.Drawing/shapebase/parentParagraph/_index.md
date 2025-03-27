---
title: ShapeBase.parentParagraph property
linktitle: parentParagraph property
articleTitle: parentParagraph property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.parentParagraph property. Returns the immediate parent paragraph."
type: docs
weight: 380
url: /nodejs-net/Aspose.Words.Drawing/shapebase/parentParagraph/
---

## ShapeBase.parentParagraph property

Returns the immediate parent paragraph.


```js
get parentParagraph(): Aspose.Words.Paragraph
```

### Remarks

For child shapes of a group shape and child shapes of an Office Math object always returns ``None``.


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

