---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words for .NET
description: DocumentBuilder MoveTo method. Moves the cursor to an inline node or to the end of a paragraph in C#.
type: docs
weight: 480
url: /net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Moves the cursor to an inline node or to the end of a paragraph.

```csharp
public void MoveTo(Node node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | Node | The node must be a paragraph or a direct child of a paragraph. |

## Remarks

When node is an inline-level node, the cursor is moved to this node and further content will be inserted before that node.

When node is a [`Paragraph`](../../paragraph/), the cursor is moved to the end of the paragraph and further content will be inserted just before the paragraph break.

When node is a block-level node but not a [`Paragraph`](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node and further content will be inserted just before the paragraph break.

## Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// The document builder has a cursor, which acts as the part of the document
// where the builder appends new nodes when we use its document construction methods.
// This cursor functions in the same way as Microsoft Word's blinking cursor,
// and it also always ends up immediately after any node that the builder just inserted.
// To append content to a different part of the document,
// we can move the cursor to a different node with the "MoveTo" method.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// The cursor is now in front of the node that we moved it to.
// Adding a second run will insert it in front of the first run.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Move the cursor to the end of the document to continue appending text to the end as before.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Shows how to move a document builder's cursor to different nodes in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
// and a bookmark end node. 
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// The document builder's cursor is always ahead of the node that we last added with it.
// If the builder's cursor is at the end of the document, its current node will be null.
// The previous node is the bookmark end node that we last added.
// Adding new nodes with the builder will append them to the last node.
Assert.Null(builder.CurrentNode);

// If we wish to edit a different part of the document with the builder,
// we will need to bring its cursor to the node we wish to edit.
builder.MoveToBookmark("MyBookmark");

// Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// We can also move the cursor to an individual node like this.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// We can use specific methods to move to the start/end of a document.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### See Also

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
