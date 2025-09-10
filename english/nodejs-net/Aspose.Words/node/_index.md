---
title: Node class
linktitle: Node class
articleTitle: Node class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Node class. Base class for all nodes of a Word document"
type: docs
weight: 830
url: /nodejs-net/aspose.words/node/
---

## Node class

Base class for all nodes of a Word document.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

A document is represented as a tree of nodes, similar to DOM or XmlDocument.

For more info see the Composite design pattern.

The [Node](./) class:


* Defines the child node interface.
  
* Defines the interface for visiting nodes.
  
* Provides default cloning capability.
  
* Implements parent node and owner document mechanisms.
  
* Implements access to sibling nodes.
  



### Properties

| Name | Description |
| --- | --- |
| [customNodeId](./customNodeId/) | Specifies custom node identifier. |
| [document](./document/) | Gets the document to which this node belongs. |
| [isComposite](./isComposite/) | Returns ``true`` if this node can contain other nodes. |
| [nextSibling](./nextSibling/) | Gets the node immediately following this node. |
| [nodeType](./nodeType/) | Gets the type of this node. |
| [parentNode](./parentNode/) | Gets the immediate parent of this node. |
| [previousSibling](./previousSibling/) | Gets the node immediately preceding this node. |
| [range](./range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |

### Methods

| Name | Description |
| --- | --- |
|[ asBody()](./asBody/#default) | Cast node to [Body](../body/). |
|[ asBookmarkEnd()](./asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/). |
|[ asBookmarkStart()](./asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/). |
|[ asBuildingBlock()](./asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/). |
|[ asCell()](./asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/). |
|[ asComment()](./asComment/#default) | Cast node to [Comment](../comment/). |
|[ asCommentRangeEnd()](./asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../commentrangeend/). |
|[ asCommentRangeStart()](./asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/). |
|[ asCompositeNode()](./asCompositeNode/#default) | Cast node to [CompositeNode](../compositenode/). |
|[ asDocument()](./asDocument/#default) | Cast node to [Node.document](./document/). |
|[ asEditableRangeEnd()](./asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../editablerangeend/). |
|[ asEditableRangeStart()](./asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../editablerangestart/). |
|[ asFieldEnd()](./asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/). |
|[ asFieldSeparator()](./asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/). |
|[ asFieldStart()](./asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/). |
|[ asFootnote()](./asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/). |
|[ asFormField()](./asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/). |
|[ asGlossaryDocument()](./asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/). |
|[ asGroupShape()](./asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/). |
|[ asHeaderFooter()](./asHeaderFooter/#default) | Cast node to [HeaderFooter](../headerfooter/). |
|[ asOfficeMath()](./asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/). |
|[ asParagraph()](./asParagraph/#default) | Cast node to [Paragraph](../paragraph/). |
|[ asRow()](./asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/). |
|[ asRun()](./asRun/#default) | Cast node to [Run](../run/). |
|[ asSection()](./asSection/#default) | Cast node to [Section](../section/). |
|[ asShape()](./asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/). |
|[ asSmartTag()](./asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/). |
|[ asSpecialChar()](./asSpecialChar/#default) | Cast node to [SpecialChar](../specialchar/). |
|[ asStructuredDocumentTag()](./asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). |
|[ asStructuredDocumentTagRangeEnd()](./asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/). |
|[ asStructuredDocumentTagRangeStart()](./asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/). |
|[ asSubDocument()](./asSubDocument/#default) | Cast node to [SubDocument](../subdocument/). |
|[ asTable()](./asTable/#default) | Cast node to [Table](../table/). |
|[ clone(isCloneChildren)](./clone/#boolean) | Creates a duplicate of the node. |
|[ getAncestor(ancestorType)](./getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
|[ getText()](./getText/#default) | Gets the text of this node and of all its children. |
|[ nextPreOrder(rootNode)](./nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm. |
|[ nodeTypeToString(nodeType)](./nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string. |
|[ previousPreOrder(rootNode)](./previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm. |
|[ referenceEquals(other)](./referenceEquals/#node) |  |
|[ remove()](./remove/#default) | Removes itself from the parent. |
|[ toString(saveFormat)](./toString/#saveformat) | Exports the content of the node into a string in the specified format. |
|[ toString(saveOptions)](./toString/#saveoptions) | Exports the content of the node into a string using the specified save options. |

### Examples

Shows how to clone a composite node.

```js
let doc = new aw.Document();
let para = doc.firstSection.body.firstParagraph;
para.appendChild(new aw.Run(doc, "Hello world!"));

// Below are two ways of cloning a composite node.
// 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
let cloneWithChildren = para.clone(true).asParagraph();

expect(cloneWithChildren.hasChildNodes).toEqual(true);
expect(cloneWithChildren.getText().trim()).toEqual("Hello world!");

// 2 -  Create a clone of a node just by itself without any children.
let cloneWithoutChildren = para.clone(false).asParagraph();

expect(cloneWithoutChildren.hasChildNodes).toEqual(false);
expect(cloneWithoutChildren.getText().trim()).toEqual('');
```

Shows how to traverse through a composite node's collection of child nodes.

```js
let doc = new aw.Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
let paragraph = doc.getParagraph(0, true);
paragraph.appendChild(new aw.Run(doc, "Hello world! "));

let shape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);
shape.width = 200;
shape.height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.customNodeId = 100;
shape.wrapType = aw.Drawing.WrapType.Inline;
paragraph.appendChild(shape);

paragraph.appendChild(new aw.Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
let children = paragraph.getChildNodes(aw.NodeType.Any, false);

expect(paragraph.getChildNodes(aw.NodeType.Any, false).count).toEqual(3);

for (let child of children)
  switch (child.nodeType)
  {
    case aw.NodeType.Run:
      console.log("Run contents:");
      console.log(`\t\"${child.getText().trim()}\"`);
      break;
    case aw.NodeType.Shape:
      let childShape = child.asShape();
      console.log("Shape:");
      console.log(`\t${childShape.shapeType}, ${childShape.width}x${childShape.height}`);
      expect(shape.customNodeId).toEqual(100);
      break;
  }
```

Shows how to remove all child nodes of a specific type from a composite node.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

expect(doc.getChildNodes(aw.NodeType.Table, true).count).toEqual(2);

let curNode = doc.firstSection.body.firstChild;

while (curNode != null)
{
  // Save the next sibling node as a variable in case we want to move to it after deleting this node.
  let nextNode = curNode.nextSibling;

  // A section body can contain Paragraph and Table nodes.
  // If the node is a Table, remove it from the parent.
  if (curNode.nodeType == aw.NodeType.Table)
    curNode.remove();

  curNode = nextNode;
}

expect(doc.getChildNodes(aw.NodeType.Table, true).count).toEqual(0);
```

### See Also

* module [Aspose.Words](../)

