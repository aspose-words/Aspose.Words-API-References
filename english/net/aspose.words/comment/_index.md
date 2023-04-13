---
title: Comment Class
linktitle: Comment
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Comment class. Represents a container for text of a comment in C#.
type: docs
weight: 220
url: /net/aspose.words/comment/
---
## Comment class

Represents a container for text of a comment.

To learn more, visit the [Working with Comments](https://docs.aspose.com/words/net/working-with-comments/) documentation article.

```csharp
public sealed class Comment : InlineStory
```

## Constructors

| Name | Description |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Initializes a new instance of the `Comment` class. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Initializes a new instance of the `Comment` class. |

## Properties

| Name | Description |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Returns the parent `Comment` object. Returns `null` for top-level comments. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Returns or sets the author name for a comment. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Gets the date and time that the comment was made. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Gets or sets flag indicating that the comment has been marked done. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Gets the first paragraph in the story. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Provides access to the font formatting of the anchor character of this object. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [Id](../../aspose.words/comment/id/) { get; } | Gets the comment identifier. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Returns or sets the initials of the user associated with a specific comment. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Returns `true` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Returns `true` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Gets the last paragraph in the story. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | Returns Comment. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Gets a collection of paragraphs that are immediate children of the story. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Retrieves the parent [`Paragraph`](../paragraph/) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Returns a collection of `Comment` objects that are immediate children of the specified comment. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | Returns Comments. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Gets a collection of tables that are immediate children of the story. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Adds a reply to this comment. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Creates navigator which can be used to traverse and read nodes. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Removes all replies to this comment. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Removes the specified child node. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Removes the specified reply to this comment. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../node/) that matches the XPath expression. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | This is a convenience method that allows to easily set text of the comment. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

A comment is an annotation which is anchored to a region of text or to a position in text. A comment can contain an arbitrary amount of block-level content.

If a `Comment` object occurs on its own, the comment is anchored to the position of the `Comment` object.

To anchor a comment to a region of text three objects are required: `Comment`, [`CommentRangeStart`](../commentrangestart/) and [`CommentRangeEnd`](../commentrangeend/). All three objects need to share the same [`Id`](./id/) value.

`Comment` is an inline-level node and can only be a child of [`Paragraph`](../paragraph/).

`Comment` can contain [`Paragraph`](../paragraph/) and [`Table`](../../aspose.words.tables/table/) child nodes.

## Examples

Shows how to add a comment to a paragraph.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Shows how to add a comment to a document, and then reply to it.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder.CurrentParagraph.AppendChild(comment);

// Add a reply, which will show up under its parent comment.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Comments and replies are both Comment nodes.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
Assert.Null(comment.Ancestor);

// Replies have an ancestor top-level comment.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### See Also

* class [InlineStory](../inlinestory/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
