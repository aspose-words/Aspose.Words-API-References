---
title: Comment class
linktitle: Comment class
articleTitle: Comment class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Comment class. Represents a container for text of a comment"
type: docs
weight: 190
url: /nodejs-net/aspose.words/comment/
---

## Comment class

Represents a container for text of a comment.
To learn more, visit the [Working with Comments](https://docs.aspose.com/words/nodejs-net/working-with-comments/) documentation article.




### Remarks

A comment is an annotation which is anchored to a region of text or to a position in text.
A comment can contain an arbitrary amount of block-level content.

If a [Comment](./) object occurs on its own, the comment is anchored to
the position of the [Comment](./) object.

To anchor a comment to a region of text three objects are required: [Comment](./),
[CommentRangeStart](../commentrangestart/) and [CommentRangeEnd](../commentrangeend/). All three objects need to share the same
[Comment.id](./id/) value.

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../table/) child nodes.




**Inheritance:** [Comment](./) → [InlineStory](../inlinestory/) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Comment(doc)](./constructor/#documentbase) | Initializes a new instance of the [Comment](./) class. |
| [Comment(doc, author, initial, dateTime)](./constructor/#documentbase_string_string_date) | Initializes a new instance of the [Comment](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [ancestor](./ancestor/) | Returns the parent [Comment](./) object. Returns ``null`` for top-level comments. |
| [author](./author/) | Returns or sets the author name for a comment. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [dateTime](./dateTime/) | Gets the date and time that the comment was made. |
| [dateTimeUtc](./dateTimeUtc/) | Gets the UTC date and time that the comment was made. |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [done](./done/) | Gets or sets flag indicating that the comment has been marked done. |
| [firstChild](../compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [firstParagraph](../inlinestory/firstParagraph/) | Gets the first paragraph in the story.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [font](../inlinestory/font/) | Provides access to the font formatting of the anchor character of this object.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [hasChildNodes](../compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [id](./id/) | Gets or sets the comment identifier. |
| [initial](./initial/) | Returns or sets the initials of the user associated with a specific comment. |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [isDeleteRevision](../inlinestory/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [isInsertRevision](../inlinestory/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [isMoveFromRevision](../inlinestory/isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [isMoveToRevision](../inlinestory/isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [lastChild](../compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [lastParagraph](../inlinestory/lastParagraph/) | Gets the last paragraph in the story.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.Comment](../nodetype/#Comment). |
| [paragraphs](../inlinestory/paragraphs/) | Gets a collection of paragraphs that are immediate children of the story.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [parentId](./parentId/) | Gets or sets the parent comment ID. A value of ``-1`` means the comment has no parent. |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parentParagraph](../inlinestory/parentParagraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node.<br>(Inherited from [InlineStory](../inlinestory/)) |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [replies](./replies/) | Returns a collection of [Comment](./) objects that are immediate children of the specified comment. |
| [storyType](./storyType/) | Returns [StoryType.Comments](../storytype/#Comments). |
| [tables](../inlinestory/tables/) | Gets a collection of tables that are immediate children of the story.<br>(Inherited from [InlineStory](../inlinestory/)) |

### Methods

| Name | Description |
| --- | --- |
|[ addReply(author, initial, dateTime, text)](./addReply/#string_string_date_string) | Adds a reply to this comment. |
|[ appendChild(newChild)](../compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ asBody()](../node/asBody/#default) | Cast node to [Body](../body/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkEnd()](../node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkStart()](../node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/).<br>(Inherited from [Node](../node/)) |
|[ asBuildingBlock()](../node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/).<br>(Inherited from [Node](../node/)) |
|[ asCell()](../node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../node/)) |
|[ asComment()](../node/asComment/#default) | Cast node to [Comment](./).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeEnd()](../node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../commentrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeStart()](../node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asCompositeNode()](../node/asCompositeNode/#default) | Cast node to [CompositeNode](../compositenode/).<br>(Inherited from [Node](../node/)) |
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
|[ ensureMinimum()](../inlinestory/ensureMinimum/#default) | If the last child is not a paragraph, creates and appends one empty paragraph.<br>(Inherited from [InlineStory](../inlinestory/)) |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getBuildingBlock(index, isDeep)](../compositenode/getBuildingBlock/#number_boolean) | Returns an Nth child [BuildingBlock](../buildingblock/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getComment(index, isDeep)](../compositenode/getComment/#number_boolean) | Returns an Nth child [Comment](./) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../compositenode/getEditableRangeStart/#number_boolean) | Returns an Nth child [EditableRangeStart](../editablerangestart/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getFootnote(index, isDeep)](../compositenode/getFootnote/#number_boolean) | Returns an Nth child [Footnote](../../aspose.words.notes/footnote/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getGroupShape(index, isDeep)](../compositenode/getGroupShape/#number_boolean) | Returns an Nth child [GroupShape](../../aspose.words.drawing/groupshape/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getOfficeMath(index, isDeep)](../compositenode/getOfficeMath/#number_boolean) | Returns an Nth child [OfficeMath](../../aspose.words.math/officemath/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getParagraph(index, isDeep)](../compositenode/getParagraph/#number_boolean) | Returns an Nth child [Paragraph](../paragraph/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getRun(index, isDeep)](../compositenode/getRun/#number_boolean) | Returns an Nth child [Run](../run/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdt(index, isDeep)](../compositenode/getSdt/#number_boolean) | Returns an Nth child [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../compositenode/getSdtRangeEnd/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../compositenode/getSdtRangeStart/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getShape(index, isDeep)](../compositenode/getShape/#number_boolean) | Returns an Nth child [Shape](../../aspose.words.drawing/shape/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSmartTag(index, isDeep)](../compositenode/getSmartTag/#number_boolean) | Returns an Nth child [SmartTag](../../aspose.words.markup/smarttag/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getTable(index, isDeep)](../compositenode/getTable/#number_boolean) | Returns an Nth child [Table](../table/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getText()](../node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ indexOf(child)](../compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertAfter(newChild, refChild)](../compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertBefore(newChild, refChild)](../compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prependChild(newChild)](../compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ removeAllChildren()](../compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeAllReplies()](./removeAllReplies/#default) | Removes all replies to this comment. |
|[ removeChild(oldChild)](../compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeReply(reply)](./removeReply/#comment) | Removes the specified reply to this comment. |
|[ removeSmartTags()](../compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectNodes(xpath)](../compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectSingleNode(xpath)](../compositenode/selectSingleNode/#string) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ setText(text)](./setText/#string) | This is a convenience method that allows to easily set text of the comment. |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to add a comment to a document, and then reply to it.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let comment = new aw.Comment(doc, "John Doe", "J.D.", Date.now());
comment.setText("My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder.currentParagraph.appendChild(comment);

// Add a reply, which will show up under its parent comment.
comment.addReply("Joe Bloggs", "J.B.", Date.now(), "New reply");

// Comments and replies are both Comment nodes.
expect(doc.getChildNodes(aw.NodeType.Comment, true).count).toEqual(2);

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
expect(comment.ancestor).toBe(null);

// Replies have an ancestor top-level comment.
expect(comment.replies.at(0).ancestor).toEqual(comment);

doc.save(base.artifactsDir + "Comment.AddCommentWithReply.docx");
```

Shows how to add a comment to a paragraph.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.write("Hello world!");

var today = new Date(2024, 11, 26);
var comment = new aw.Comment(doc, "John Doe", "JD", today);
builder.currentParagraph.appendChild(comment);
builder.moveTo(comment.appendChild(new aw.Paragraph(doc)));
builder.write("Comment text.");

expect(comment.dateTime).toEqual(today);

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it. 
doc.save(base.artifactsDir + "InlineStory.AddComment.docx");
```

### See Also

* module [Aspose.Words](../)
* class [InlineStory](../inlinestory/)
* class [CommentRangeStart](../commentrangestart/)
* class [CommentRangeEnd](../commentrangeend/)

