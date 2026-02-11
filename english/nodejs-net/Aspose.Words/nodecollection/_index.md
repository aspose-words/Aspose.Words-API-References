---
title: NodeCollection class
linktitle: NodeCollection class
articleTitle: NodeCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.NodeCollection class. Represents a collection of nodes of a specific type"
type: docs
weight: 880
url: /nodejs-net/aspose.words/nodecollection/
---

## NodeCollection class

Represents a collection of nodes of a specific type.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

[NodeCollection](./) does not own the nodes it contains, rather, is just a selection of nodes
of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](./) supports indexed access, iteration and provides add and remove methods.

The [NodeCollection](./) collection is "live", i.e. changes to the children of the node object
that it was created from are immediately reflected in the nodes returned by the [NodeCollection](./)
properties and methods.

[NodeCollection](./) is returned by [CompositeNode.getChildNodes()](../compositenode/getChildNodes/#nodetype_boolean)
and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/),
[ParagraphCollection](../paragraphcollection/) etc.

[NodeCollection](./) can be "flat" and contain only immediate children of the node it was created
from, or it can be "deep" and contain all descendant children.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of nodes in the collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](./add/#node) | Adds a node to the end of the collection. |
|[ clear()](./clear/#default) | Removes all nodes from this collection and from the document. |
|[ contains(node)](./contains/#node) | Determines whether a node is in the collection. |
|[ indexOf(node)](./indexOf/#node) | Returns the zero-based index of the specified node. |
|[ insert(index, node)](./insert/#number_node) | Inserts a node into the collection at the specified index. |
|[ remove(node)](./remove/#node) | Removes the node from the collection and from the document. |
|[ removeAt(index)](./removeAt/#number) | Removes the node at the specified index from the collection and from the document. |
|[ toArray()](./toArray/#default) | Copies all nodes from the collection to a new array of nodes. |

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

* module [Aspose.Words](../)

