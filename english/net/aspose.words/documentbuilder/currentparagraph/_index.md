---
title: DocumentBuilder.CurrentParagraph
linktitle: CurrentParagraph
articleTitle: CurrentParagraph
second_title: Aspose.Words for .NET
description: Access the selected paragraph in DocumentBuilder easily with the CurrentParagraph property. Streamline your document editing process today!
type: docs
weight: 50
url: /net/aspose.words/documentbuilder/currentparagraph/
---
## DocumentBuilder.CurrentParagraph property

Gets the paragraph that is currently selected in this [`DocumentBuilder`](../).

```csharp
public Paragraph CurrentParagraph { get; }
```

## Remarks

[`CurrentNode`](../currentnode/)

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

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
