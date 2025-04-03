---
title: CompositeNode class
linktitle: CompositeNode class
articleTitle: CompositeNode class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.CompositeNode class. Base class for nodes that can contain other nodes"
type: docs
weight: 230
url: /nodejs-net/Aspose.Words/compositenode/
---

## CompositeNode class

Base class for nodes that can contain other nodes.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

A document is represented as a tree of nodes, similar to DOM or XmlDocument.

For more info see the Composite design pattern.

The [CompositeNode](./) class:


* Provides access to the child nodes.
  
* Implements Composite operations such as insert and remove children.
  
* Provides methods for XPath navigation.
  



**Inheritance:** [CompositeNode](./) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of immediate children of this node. |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [firstChild](./firstChild/) | Gets the first child of the node. |
| [hasChildNodes](./hasChildNodes/) | Returns ``true`` if this node has any child nodes. |
| [isComposite](./isComposite/) | Returns ``true`` as this node can have child nodes. |
| [lastChild](./lastChild/) | Gets the last child of the node. |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](../node/nodeType/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
|[ appendChild(newChild)](./appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node. |
|[ asBody()](../node/asBody/#default) | Cast node to [Body](../body/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkEnd()](../node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkStart()](../node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/).<br>(Inherited from [Node](../node/)) |
|[ asBuildingBlock()](../node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/).<br>(Inherited from [Node](../node/)) |
|[ asCell()](../node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../node/)) |
|[ asComment()](../node/asComment/#default) | Cast node to [Comment](../comment/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeEnd()](../node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../commentrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeStart()](../node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asCompositeNode()](../node/asCompositeNode/#default) | Cast node to [CompositeNode](./).<br>(Inherited from [Node](../node/)) |
|[ asDocument()](../node/asDocument/#default) | Cast node to [Node.document](../node/document/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeEnd()](../node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../editablerangeend/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeStart()](../node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../editablerangestart/).<br>(Inherited from [Node](../node/)) |
|[ asFieldEnd()](../node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../node/)) |
|[ asFieldSeparator()](../node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../node/)) |
|[ asFieldStart()](../node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../node/)) |
|[ asFootnote()](../node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../node/)) |
|[ asFormField()](../node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../node/)) |
|[ asGlossaryDocument()](../node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../node/)) |
|[ asGroupShape()](../node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../node/)) |
|[ asHeaderFooter()](../node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../headerfooter/).<br>(Inherited from [Node](../node/)) |
|[ asOfficeMath()](../node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../node/)) |
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](../paragraph/).<br>(Inherited from [Node](../node/)) |
|[ asRow()](../node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../node/)) |
|[ asRun()](../node/asRun/#default) | Cast node to [Run](../run/).<br>(Inherited from [Node](../node/)) |
|[ asSection()](../node/asSection/#default) | Cast node to [Section](../section/).<br>(Inherited from [Node](../node/)) |
|[ asShape()](../node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../node/)) |
|[ asSmartTag()](../node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../node/)) |
|[ asSpecialChar()](../node/asSpecialChar/#default) | Cast node to [SpecialChar](../specialchar/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTag()](../node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeEnd()](../node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeStart()](../node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asSubDocument()](../node/asSubDocument/#default) | Cast node to [SubDocument](../subdocument/).<br>(Inherited from [Node](../node/)) |
|[ asTable()](../node/asTable/#default) | Cast node to [Table](../table/).<br>(Inherited from [Node](../node/)) |
|[ clone(isCloneChildren)](../node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getBuildingBlock(index, isDeep)](./getBuildingBlock/#number_boolean) |  |
|[ getChild(nodeType, index, isDeep)](./getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type. |
|[ getChildNodes(nodeType, isDeep)](./getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type. |
|[ getComment(index, isDeep)](./getComment/#number_boolean) |  |
|[ getEditableRangeStart(index, isDeep)](./getEditableRangeStart/#number_boolean) |  |
|[ getFootnote(index, isDeep)](./getFootnote/#number_boolean) |  |
|[ getGroupShape(index, isDeep)](./getGroupShape/#number_boolean) |  |
|[ getOfficeMath(index, isDeep)](./getOfficeMath/#number_boolean) |  |
|[ getParagraph(index, isDeep)](./getParagraph/#number_boolean) |  |
|[ getRun(index, isDeep)](./getRun/#number_boolean) |  |
|[ getSdt(index, isDeep)](./getSdt/#number_boolean) |  |
|[ getSdtRangeEnd(index, isDeep)](./getSdtRangeEnd/#number_boolean) |  |
|[ getSdtRangeStart(index, isDeep)](./getSdtRangeStart/#number_boolean) |  |
|[ getShape(index, isDeep)](./getShape/#number_boolean) |  |
|[ getSmartTag(index, isDeep)](./getSmartTag/#number_boolean) |  |
|[ getTable(index, isDeep)](./getTable/#number_boolean) |  |
|[ getText()](./getText/#default) | Gets the text of this node and of all its children. |
|[ indexOf(child)](./indexOf/#node) | Returns the index of the specified child node in the child node array. |
|[ insertAfter(newChild, refChild)](./insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node. |
|[ insertBefore(newChild, refChild)](./insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node. |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prependChild(newChild)](./prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node. |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ removeAllChildren()](./removeAllChildren/#default) | Removes all the child nodes of the current node. |
|[ removeChild(oldChild)](./removeChild/#node) | Removes the specified child node. |
|[ removeSmartTags()](./removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
|[ selectNodes(xpath)](./selectNodes/#string) | Selects a list of nodes matching the XPath expression. |
|[ selectSingleNode(xpath)](./selectSingleNode/#string) | Selects the first [Node](../node/) that matches the XPath expression. |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

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

### See Also

* module [Aspose.Words](../)
* class [Node](../node/)

