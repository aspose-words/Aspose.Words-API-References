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

Can be immediate child of [Body](../../Aspose.Words/body/) node **only**.



**Inheritance:** [StructuredDocumentTagRangeStart](./) → [Node](../../Aspose.Words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [StructuredDocumentTagRangeStart(doc, type)](./StructuredDocumentTagRangeStart/#documentbase_sdttype) | Initializes a new instance of the **Structured document tag range start** class. |

### Properties

| Name | Description |
| --- | --- |
| [appearance](./appearance/) | Gets or sets the appearance of the structured document tag. |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [isShowingPlaceholderText](./isShowingPlaceholderText/) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [lastChild](./lastChild/) | Gets the last child in the stdContent range. |
| [level](./level/) | Gets the level at which this structured document tag range start occurs in the document tree. |
| [lockContentControl](./lockContentControl/) | When set to ``True``, this property will prohibit a user from deleting this structured document tag. |
| [lockContents](./lockContents/) | When set to ``True``, this property will prohibit a user from editing the contents of this structured document tag. |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.StructuredDocumentTagRangeStart](../../Aspose.Words/nodetype/#StructuredDocumentTagRangeStart). |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../Aspose.Words/buildingblock/) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [StructuredDocumentTagRangeStart.xmlMapping](./xmlMapping/) element or the [StructuredDocumentTagRangeStart.isShowingPlaceholderText](./isShowingPlaceholderText/) element is ``True``. |
| [placeholderName](./placeholderName/) | Gets or sets Name of the [BuildingBlock](../../Aspose.Words/buildingblock/) containing placeholder text. |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [rangeEnd](./rangeEnd/) | Specifies end of range if the [StructuredDocumentTag](../structureddocumenttag/) is a ranged structured document tag. Otherwise returns ``None``. |
| [sdtType](./sdtType/) | Gets type of this structured document tag. |
| [tag](./tag/) | Specifies a tag associated with the current structured document tag node. Can not be ``None``. |
| [title](./title/) | Specifies the friendly name associated with this structured document tag. Can not be ``None``. |
| [wordOpenXML](./wordOpenXML/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../Aspose.Words/saveformat/#FlatOpc) format. |
| [wordOpenXMLMinimal](./wordOpenXMLMinimal/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../Aspose.Words/saveformat/#FlatOpc) format. |
| [xmlMapping](./xmlMapping/) | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ appendChild(newChild)](./appendChild/#node) | Adds the specified node to the end of the stdContent range. |
|[ asBody()](../../Aspose.Words/node/asBody/#default) | Cast node to [Body](../../Aspose.Words/body/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkEnd()](../../Aspose.Words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../Aspose.Words/bookmarkend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkStart()](../../Aspose.Words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../Aspose.Words/bookmarkstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBuildingBlock()](../../Aspose.Words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../Aspose.Words/buildingblock/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCell()](../../Aspose.Words/node/asCell/#default) | Cast node to [Cell](../../Aspose.Words.Tables/cell/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asComment()](../../Aspose.Words/node/asComment/#default) | Cast node to [Comment](../../Aspose.Words/comment/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeEnd()](../../Aspose.Words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../Aspose.Words/commentrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeStart()](../../Aspose.Words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../Aspose.Words/commentrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCompositeNode()](../../Aspose.Words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../Aspose.Words/compositenode/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asDocument()](../../Aspose.Words/node/asDocument/#default) | Cast node to [Node.document](../../Aspose.Words/node/document/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeEnd()](../../Aspose.Words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../Aspose.Words/editablerangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeStart()](../../Aspose.Words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../Aspose.Words/editablerangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldEnd()](../../Aspose.Words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../../Aspose.Words.Fields/fieldend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldSeparator()](../../Aspose.Words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../Aspose.Words.Fields/fieldseparator/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldStart()](../../Aspose.Words/node/asFieldStart/#default) | Cast node to [FieldStart](../../Aspose.Words.Fields/fieldstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFootnote()](../../Aspose.Words/node/asFootnote/#default) | Cast node to [Footnote](../../Aspose.Words.Notes/footnote/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFormField()](../../Aspose.Words/node/asFormField/#default) | Cast node to [FormField](../../Aspose.Words.Fields/formfield/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGlossaryDocument()](../../Aspose.Words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../Aspose.Words.BuildingBlocks/glossarydocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](../smarttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../structureddocumenttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](./).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSubDocument()](../../Aspose.Words/node/asSubDocument/#default) | Cast node to [SubDocument](../../Aspose.Words/subdocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asTable()](../../Aspose.Words/node/asTable/#default) | Cast node to [Table](../../Aspose.Words/table/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ clone(isCloneChildren)](../../Aspose.Words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getAncestor(ancestorType)](../../Aspose.Words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../Aspose.Words/nodetype/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getChildNodes(nodeType, isDeep)](./getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified types. |
|[ getText()](../../Aspose.Words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nextPreOrder(rootNode)](../../Aspose.Words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nodeTypeToString(nodeType)](../../Aspose.Words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ previousPreOrder(rootNode)](../../Aspose.Words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ referenceEquals(other)](../../Aspose.Words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ remove()](../../Aspose.Words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ removeAllChildren()](./removeAllChildren/#default) | Removes all the nodes between this range start node and the range end node. |
|[ removeSelfOnly()](./removeSelfOnly/#default) | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

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
* class [Node](../../Aspose.Words/node/)

