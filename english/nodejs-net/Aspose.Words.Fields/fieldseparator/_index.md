---
title: FieldSeparator class
linktitle: FieldSeparator class
articleTitle: FieldSeparator class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.FieldSeparator class. Represents a Word field separator that separates the field code from the field result"
type: docs
weight: 910
url: /nodejs-net/Aspose.Words.Fields/fieldseparator/
---

## FieldSeparator class

Represents a Word field separator that separates the field code from the field result.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/nodejs-net/working-with-fields/) documentation article.




### Remarks

[FieldSeparator](./) is an inline-level node and represented
by the Aspose.Words.ControlChar.FieldSeparatorChar control character in the document.

[FieldSeparator](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of
a field start character, field code, field separator character, field result
and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField()](../../aspose.words/documentbuilder/insertField/#string)
method.




**Inheritance:** [FieldSeparator](./) → [FieldChar](../fieldchar/) → [SpecialChar](../../aspose.words/specialchar/) → [Inline](../../aspose.words/inline/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [fieldType](../fieldchar/fieldType/) | Returns the type of the field.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [font](../../aspose.words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [isDeleteRevision](../../aspose.words/inline/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isDirty](../fieldchar/isDirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [FieldChar](../fieldchar/)) |
| [isFormatRevision](../../aspose.words/inline/isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isInsertRevision](../../aspose.words/inline/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isLocked](../fieldchar/isLocked/) | Gets or sets whether the parent field is locked (should not recalculate its result).<br>(Inherited from [FieldChar](../fieldchar/)) |
| [isMoveFromRevision](../../aspose.words/inline/isMoveFromRevision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [isMoveToRevision](../../aspose.words/inline/isMoveToRevision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.FieldSeparator](../../aspose.words/nodetype/#FieldSeparator). |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parentParagraph](../../aspose.words/inline/parentParagraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
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
|[ asFieldEnd()](../../aspose.words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../fieldend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldSeparator()](../../aspose.words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldStart()](../../aspose.words/node/asFieldStart/#default) | Cast node to [FieldStart](../fieldstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFootnote()](../../aspose.words/node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFormField()](../../aspose.words/node/asFormField/#default) | Cast node to [FormField](../formfield/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGlossaryDocument()](../../aspose.words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSubDocument()](../../aspose.words/node/asSubDocument/#default) | Cast node to [SubDocument](../../aspose.words/subdocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asTable()](../../aspose.words/node/asTable/#default) | Cast node to [Table](../../aspose.words/table/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ clone(isCloneChildren)](../../aspose.words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getAncestor(ancestorType)](../../aspose.words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getField()](../fieldchar/getField/#default) | Returns a field for the field char.<br>(Inherited from [FieldChar](../fieldchar/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### See Also

* module [Aspose.Words.Fields](../)
* class [FieldChar](../fieldchar/)

