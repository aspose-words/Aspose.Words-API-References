---
title: StructuredDocumentTagRangeStart class
linktitle: StructuredDocumentTagRangeStart class
articleTitle: StructuredDocumentTagRangeStart class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.StructuredDocumentTagRangeStart class. Represents a start of ranged structured document tag which accepts multi-sections content"
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagrangestart/
---

## StructuredDocumentTagRangeStart class

Represents a start of **ranged** structured document tag which accepts multi-sections content.
See also [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Remarks

Can be immediate child of [Body](../../aspose.words/body/) node **only**.



**Inheritance:** [StructuredDocumentTagRangeStart](./) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [StructuredDocumentTagRangeStart(doc, type)](./constructor/#documentbase_sdttype) | Initializes a new instance of the **Structured document tag range start** class. |

### Properties

| Name | Description |
| --- | --- |
| [appearance](./appearance/) | Gets or sets the appearance of the structured document tag. |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [isShowingPlaceholderText](./isShowingPlaceholderText/) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [lastChild](./lastChild/) | Gets the last child in the stdContent range. |
| [level](./level/) | Gets the level at which this structured document tag range start occurs in the document tree. |
| [lockContentControl](./lockContentControl/) | When set to ``True``, this property will prohibit a user from deleting this structured document tag. |
| [lockContents](./lockContents/) | When set to ``True``, this property will prohibit a user from editing the contents of this structured document tag. |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.StructuredDocumentTagRangeStart](../../aspose.words/nodetype/#StructuredDocumentTagRangeStart). |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../aspose.words/buildingblock/) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [StructuredDocumentTagRangeStart.xmlMapping](./xmlMapping/) element or the [StructuredDocumentTagRangeStart.isShowingPlaceholderText](./isShowingPlaceholderText/) element is ``True``. |
| [placeholderName](./placeholderName/) | Gets or sets Name of the [BuildingBlock](../../aspose.words/buildingblock/) containing placeholder text. |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [rangeEnd](./rangeEnd/) | Specifies end of range if the [StructuredDocumentTag](../structureddocumenttag/) is a ranged structured document tag. Otherwise returns ``None``. |
| [sdtType](./sdtType/) | Gets type of this structured document tag. |
| [tag](./tag/) | Specifies a tag associated with the current structured document tag node. Can not be ``None``. |
| [title](./title/) | Specifies the friendly name associated with this structured document tag. Can not be ``None``. |
| [wordOpenXML](./wordOpenXML/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc) format. |
| [wordOpenXMLMinimal](./wordOpenXMLMinimal/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc) format. |
| [xmlMapping](./xmlMapping/) | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ appendChild(newChild)](./appendChild/#node) | Adds the specified node to the end of the stdContent range. |
|[ asBody()](../../aspose.words/node/asBody/#default) | Cast node to [Body](../../aspose.words/body/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkEnd()](../../aspose.words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../aspose.words/bookmarkend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkStart()](../../aspose.words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../aspose.words/bookmarkstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBuildingBlock()](../../aspose.words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../aspose.words/buildingblock/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCell()](../../aspose.words/node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asComment()](../../aspose.words/node/asComment/#default) | Cast node to [Comment](../../aspose.words/comment/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeEnd()](../../aspose.words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../aspose.words/commentrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeStart()](../../aspose.words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../aspose.words/commentrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCompositeNode()](../../aspose.words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../aspose.words/compositenode/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asDocument()](../../aspose.words/node/asDocument/#default) | Cast node to [Node.document](../../aspose.words/node/document/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeEnd()](../../aspose.words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../aspose.words/editablerangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeStart()](../../aspose.words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../aspose.words/editablerangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldEnd()](../../aspose.words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldSeparator()](../../aspose.words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldStart()](../../aspose.words/node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFootnote()](../../aspose.words/node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFormField()](../../aspose.words/node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGlossaryDocument()](../../aspose.words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](../smarttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSubDocument()](../../aspose.words/node/asSubDocument/#default) | Cast node to [SubDocument](../../aspose.words/subdocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asTable()](../../aspose.words/node/asTable/#default) | Cast node to [Table](../../aspose.words/table/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ clone(isCloneChildren)](../../aspose.words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getAncestor(ancestorType)](../../aspose.words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getChildNodes(nodeType, isDeep)](./getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified types. |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ removeAllChildren()](./removeAllChildren/#default) | Removes all the nodes between this range start node and the range end node. |
|[ removeSelfOnly()](./removeSelfOnly/#default) | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to get the properties of multi-section structured document tags.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");

let rangeStartTag = doc.getChildNodes(aw.NodeType.StructuredDocumentTagRangeStart, true).at(0).asStructuredDocumentTagRangeStart();
let rangeEndTag = doc.getChildNodes(aw.NodeType.StructuredDocumentTagRangeEnd, true).at(0).asStructuredDocumentTagRangeEnd();

expect(rangeEndTag.id).toEqual(rangeStartTag.id);
expect(rangeStartTag.nodeType).toEqual(aw.NodeType.StructuredDocumentTagRangeStart);
expect(rangeEndTag.nodeType).toEqual(aw.NodeType.StructuredDocumentTagRangeEnd);

console.log("StructuredDocumentTagRangeStart values:");
console.log(`\t|Id: ${rangeStartTag.id}`);
console.log(`\t|Title: ${rangeStartTag.title}`);
console.log(`\t|PlaceholderName: ${rangeStartTag.placeholderName}`);
console.log(`\t|IsShowingPlaceholderText: ${rangeStartTag.isShowingPlaceholderText}`);
console.log(`\t|LockContentControl: ${rangeStartTag.lockContentControl}`);
console.log(`\t|LockContents: ${rangeStartTag.lockContents}`);
console.log(`\t|Level: ${rangeStartTag.level}`);
console.log(`\t|NodeType: ${rangeStartTag.nodeType}`);
console.log(`\t|RangeEnd.NodeType: ${rangeStartTag.rangeEnd.nodeType}`);
console.log(`\t|Color: ${rangeStartTag.color}`);
console.log(`\t|SdtType: ${rangeStartTag.sdtType}`);
console.log(`\t|FlatOpcContent: ${rangeStartTag.wordOpenXML}`);
console.log(`\t|Tag: ${rangeStartTag.tag}\n`);

console.log("StructuredDocumentTagRangeEnd values:");
console.log(`\t|Id: ${rangeEndTag.id}`);
console.log(`\t|NodeType: ${rangeEndTag.nodeType}`);
```

### See Also

* module [Aspose.Words.Markup](../)
* class [Node](../../aspose.words/node/)

