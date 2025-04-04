---
title: ShapeBase.wrapSide property
linktitle: wrapSide property
articleTitle: wrapSide property
second_title: Aspose.Words for Node.js
description: "ShapeBase.wrapSide property. Specifies how the text is wrapped around the shape."
type: docs
weight: 570
url: /nodejs-net/aspose.words.drawing/shapebase/wrapSide/
---

## ShapeBase.wrapSide property

Specifies how the text is wrapped around the shape.


```js
get wrapSide(): Aspose.Words.Drawing.WrapSide
```

### Remarks

The default value is [WrapSide.Both](../../wrapside/#Both).

Has effect only for top level shapes.




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

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

