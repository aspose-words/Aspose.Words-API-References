---
title: InlineStory Class
linktitle: InlineStory
articleTitle: InlineStory
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.InlineStory class, the essential base for inline nodes, enabling seamless integration of paragraphs and tables in your documents.
type: docs
weight: 3750
url: /net/aspose.words/inlinestory/
---
## InlineStory class

Base class for inline-level nodes that can contain paragraphs and tables.

To learn more, visit the [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) documentation article.

```csharp
public abstract class InlineStory : CompositeNode
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Gets the first paragraph in the story. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Provides access to the font formatting of the anchor character of this object. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Returns `true` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Returns `true` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Gets the last paragraph in the story. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Gets the type of this node. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Gets a collection of paragraphs that are immediate children of the story. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Retrieves the parent [`Paragraph`](../paragraph/) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | Returns the type of the story. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Gets a collection of tables that are immediate children of the story. |

## Methods

| Name | Description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Adds the specified node to the end of the list of child nodes for this node. |
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
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../node/) that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

`InlineStory` is a container for block-level nodes [`Paragraph`](../paragraph/) and [`Table`](../../aspose.words.tables/table/).

The classes that derive from `InlineStory` are inline-level nodes that can contain their own text (paragraphs and tables). For example, a [`Comment`](../comment/) node contains text of a comment and a [`Footnote`](../../aspose.words.notes/footnote/) contains text of a footnote.

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

Assert.That(comment.DateTime, Is.EqualTo(DateTime.Today));

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Shows how to insert and customize footnotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
Assert.That(footnote.IsAuto, Is.True);

// We can move the document builder inside the footnote to edit its reference text. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.That(footnote.GetText().Trim(), Is.EqualTo("\u0002 Footnote text. More text added by a DocumentBuilder."));

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote.ReferenceMark = "RefMark";

Assert.That(footnote.IsAuto, Is.False);

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.That(footnote.IsAuto, Is.True);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### See Also

* class [CompositeNode](../compositenode/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
