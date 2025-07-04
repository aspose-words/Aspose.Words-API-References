---
title: DocumentBuilder.CurrentNode
linktitle: CurrentNode
articleTitle: CurrentNode
second_title: Aspose.Words for .NET
description: Discover the DocumentBuilder CurrentNode property to easily access the selected node, enhancing your document editing efficiency and workflow.
type: docs
weight: 40
url: /net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Gets the node that is currently selected in this DocumentBuilder.

```csharp
public Node CurrentNode { get; }
```

## Remarks

`CurrentNode` is a cursor of [`DocumentBuilder`](../) and points to a [`Node`](../../node/) that is a direct child of a [`Paragraph`](../../paragraph/). Any insert operations you perform using [`DocumentBuilder`](../) will insert before the `CurrentNode`.

When the current paragraph is empty or the cursor is positioned just before the end of a paragraph or structured document tag, `CurrentNode` returns `null`.

## Examples

Shows how to move a document builder's cursor to different nodes in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
// and a bookmark end node.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.That(firstParagraphNodes[0].NodeType, Is.EqualTo(NodeType.BookmarkStart));
Assert.That(firstParagraphNodes[1].NodeType, Is.EqualTo(NodeType.Run));
Assert.That(firstParagraphNodes[1].GetText().Trim(), Is.EqualTo("Bookmark contents."));
Assert.That(firstParagraphNodes[2].NodeType, Is.EqualTo(NodeType.BookmarkEnd));

// The document builder's cursor is always ahead of the node that we last added with it.
// If the builder's cursor is at the end of the document, its current node will be null.
// The previous node is the bookmark end node that we last added.
// Adding new nodes with the builder will append them to the last node.
Assert.That(builder.CurrentNode, Is.Null);

// If we wish to edit a different part of the document with the builder,
// we will need to bring its cursor to the node we wish to edit.
builder.MoveToBookmark("MyBookmark");

// Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
Assert.That(builder.CurrentNode, Is.EqualTo(firstParagraphNodes[1]));

// We can also move the cursor to an individual node like this.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.That(builder.CurrentNode.NodeType, Is.EqualTo(NodeType.BookmarkStart));
Assert.That(builder.CurrentParagraph, Is.EqualTo(doc.FirstSection.Body.FirstParagraph));
Assert.That(builder.IsAtStartOfParagraph, Is.True);

// We can use specific methods to move to the start/end of a document.
builder.MoveToDocumentEnd();

Assert.That(builder.IsAtEndOfParagraph, Is.True);

builder.MoveToDocumentStart();

Assert.That(builder.IsAtStartOfParagraph, Is.True);
```

### See Also

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
