---
title: NodeCollection.toArray method
linktitle: toArray method
articleTitle: toArray method
second_title: Aspose.Words for NodeJs
description: "NodeCollection.toArray method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/nodecollection/toArray/
---

## toArray() {#default}

Copies all nodes from the collection to a new array of nodes.


```js
toArray()
```

### Remarks

You should not be adding/removing nodes while iterating over a collection 
of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy 
nodes into a fixed-size array and then iterate over the array.




### Returns

An array of nodes.


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

* module [Aspose.Words](../../)
* class [NodeCollection](../)

