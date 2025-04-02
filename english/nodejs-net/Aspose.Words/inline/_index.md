---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 640
url: /nodejs-net/Aspose.Words/inline/
---

## Inline class

Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own.
To learn more, visit the [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/nodejs-net/logical-levels-of-nodes-in-a-document/) documentation article.




### Remarks

A class derived from [Inline](./) can be a child of [Paragraph](../paragraph/).




**Inheritance:** [Inline](./) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [font](./font/) | Provides access to the font formatting of this object. |
| [isComposite](../node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [isDeleteRevision](./isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isFormatRevision](./isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [isInsertRevision](./isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision](./isMoveFromRevision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision](./isMoveToRevision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](../node/nodeType/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parentParagraph](./parentParagraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ asBody()](../node/asBody/#default) | Cast node to [Body](../body/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkEnd()](../node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkStart()](../node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/).<br>(Inherited from [Node](../node/)) |
|[ asBuildingBlock()](../node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/).<br>(Inherited from [Node](../node/)) |
|[ asCell()](../node/asCell/#default) | Cast node to [Cell](../../Aspose.Words.Tables/cell/).<br>(Inherited from [Node](../node/)) |
|[ asComment()](../node/asComment/#default) | Cast node to [Comment](../comment/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeEnd()](../node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../commentrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeStart()](../node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asCompositeNode()](../node/asCompositeNode/#default) | Cast node to [CompositeNode](../compositenode/).<br>(Inherited from [Node](../node/)) |
|[ asDocument()](../node/asDocument/#default) | Cast node to [Node.document](../node/document/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeEnd()](../node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../editablerangeend/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeStart()](../node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../editablerangestart/).<br>(Inherited from [Node](../node/)) |
|[ asFieldEnd()](../node/asFieldEnd/#default) | Cast node to [FieldEnd](../../Aspose.Words.Fields/fieldend/).<br>(Inherited from [Node](../node/)) |
|[ asFieldSeparator()](../node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../Aspose.Words.Fields/fieldseparator/).<br>(Inherited from [Node](../node/)) |
|[ asFieldStart()](../node/asFieldStart/#default) | Cast node to [FieldStart](../../Aspose.Words.Fields/fieldstart/).<br>(Inherited from [Node](../node/)) |
|[ asFootnote()](../node/asFootnote/#default) | Cast node to [Footnote](../../Aspose.Words.Notes/footnote/).<br>(Inherited from [Node](../node/)) |
|[ asFormField()](../node/asFormField/#default) | Cast node to [FormField](../../Aspose.Words.Fields/formfield/).<br>(Inherited from [Node](../node/)) |
|[ asGlossaryDocument()](../node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../Aspose.Words.BuildingBlocks/glossarydocument/).<br>(Inherited from [Node](../node/)) |
|[ asGroupShape()](../node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../node/)) |
|[ asHeaderFooter()](../node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../headerfooter/).<br>(Inherited from [Node](../node/)) |
|[ asOfficeMath()](../node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../node/)) |
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](../paragraph/).<br>(Inherited from [Node](../node/)) |
|[ asRow()](../node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../node/)) |
|[ asRun()](../node/asRun/#default) | Cast node to [Run](../run/).<br>(Inherited from [Node](../node/)) |
|[ asSection()](../node/asSection/#default) | Cast node to [Section](../section/).<br>(Inherited from [Node](../node/)) |
|[ asShape()](../node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../node/)) |
|[ asSmartTag()](../node/asSmartTag/#default) | Cast node to [SmartTag](../../Aspose.Words.Markup/smarttag/).<br>(Inherited from [Node](../node/)) |
|[ asSpecialChar()](../node/asSpecialChar/#default) | Cast node to [SpecialChar](../specialchar/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTag()](../node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../Aspose.Words.Markup/structureddocumenttag/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeEnd()](../node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../Aspose.Words.Markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeStart()](../node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../Aspose.Words.Markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asSubDocument()](../node/asSubDocument/#default) | Cast node to [SubDocument](../subdocument/).<br>(Inherited from [Node](../node/)) |
|[ asTable()](../node/asTable/#default) | Cast node to [Table](../table/).<br>(Inherited from [Node](../node/)) |
|[ clone(isCloneChildren)](../node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getText()](../node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to determine the revision type of an inline node.

```js
let doc = new aw.Document(base.myDir + "Revision runs.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to change the proposed change effectively.
expect(doc.revisions.count).toEqual(6);

// The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
let run = doc.revisions.at(0).parentNode.asRun();

let firstParagraph = run.parentParagraph;
let runs = firstParagraph.runs.toArray();

expect(runs.length).toEqual(6);

// Below are five types of revisions that can flag an Inline node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
expect(runs.at(2).isInsertRevision).toEqual(true);

// 2 -  A "format" revision:
// This revision occurs when we change the formatting of text while tracking changes.
expect(runs.at(2).isFormatRevision).toEqual(true);

// 3 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
expect(runs.at(4).isMoveFromRevision).toEqual(true);

// 4 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
expect(runs.at(1).isMoveToRevision).toEqual(true);

// 5 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
expect(runs.at(5).isDeleteRevision).toEqual(true);
```

### See Also

* module [Aspose.Words](../)
* class [Node](../node/)

