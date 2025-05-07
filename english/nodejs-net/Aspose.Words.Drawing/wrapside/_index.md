---
title: WrapSide enumeration
linktitle: WrapSide enumeration
articleTitle: WrapSide enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.WrapSide enumeration. Specifies what side(s) of the shape or picture the text wraps around."
type: docs
weight: 530
url: /nodejs-net/aspose.words.drawing/wrapside/
---

## WrapSide enumeration

Specifies what side(s) of the shape or picture the text wraps around.


### Members

| Name | Description |
| --- | --- |
| Both | The document text wraps on both sides of the shape. |
| Left | The document text wraps on the left side of the shape only. There is a text free area on the right of the shape. |
| Right | The document text wraps on the right side of the shape only. There is a text free area on the left side of the shape. |
| Largest | The document text wraps on the side of the shape that is farthest from the page margin, leaving text free area on the other side of the shape. |
| Default | Default value is [WrapSide.Both](./#Both). |

### Examples

Shows how to replace all textbox shapes with image shapes.

```js
let doc = new aw.Document(base.myDir + "Textboxes in drawing canvas.docx");

let shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());

expect(shapes.filter(s => s.shapeType == aw.Drawing.ShapeType.TextBox).length).toEqual(3);
expect(shapes.filter(s => s.shapeType == aw.Drawing.ShapeType.Image).length).toEqual(1);

for (let shape of shapes)
{
  if (shape.shapeType == aw.Drawing.ShapeType.TextBox)
  {
    let replacementShape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Image);
    replacementShape.imageData.setImage(base.imageDir + "Logo.jpg");
    replacementShape.left = shape.left;
    replacementShape.top = shape.top;
    replacementShape.width = shape.width;
    replacementShape.height = shape.height;
    replacementShape.relativeHorizontalPosition = shape.relativeHorizontalPosition;
    replacementShape.relativeVerticalPosition = shape.relativeVerticalPosition;
    replacementShape.horizontalAlignment = shape.horizontalAlignment;
    replacementShape.verticalAlignment = shape.verticalAlignment;
    replacementShape.wrapType = shape.wrapType;
    replacementShape.wrapSide = shape.wrapSide;

    shape.parentNode.insertAfter(replacementShape, shape);
    shape.remove();
  }
}

shapes = doc.getChildNodes(aw.NodeType.Shape, true).toArray().map(node => node.asShape());

expect(shapes.filter(s => s.shapeType == aw.Drawing.ShapeType.TextBox).length).toEqual(0);
expect(shapes.filter(s => s.shapeType == aw.Drawing.ShapeType.Image).length).toEqual(4);

doc.save(base.artifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### See Also

* module [Aspose.Words.Drawing](../)
* property [ShapeBase.wrapSide](../shapebase/wrapSide/)

