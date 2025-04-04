---
title: DocumentBuilder.currentNode property
linktitle: currentNode property
articleTitle: currentNode property
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.currentNode property. Gets the node that is currently selected in this DocumentBuilder."
type: docs
weight: 40
url: /nodejs-net/aspose.words/documentbuilder/currentNode/
---

## DocumentBuilder.currentNode property

Gets the node that is currently selected in this DocumentBuilder.


```js
get currentNode(): Aspose.Words.Node
```

### Remarks

[DocumentBuilder.currentNode](./) is a cursor of [DocumentBuilder](../) and points to a [Node](../../node/)
that is a direct child of a [Paragraph](../../paragraph/). Any insert operations you perform using
[DocumentBuilder](../) will insert before the [DocumentBuilder.currentNode](./).

When the current paragraph is empty or the cursor is positioned just
before the end of a paragraph or structured document tag, [DocumentBuilder.currentNode](./) returns ``null``.




### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
// and a bookmark end node. 
builder.startBookmark("MyBookmark");
builder.write("Bookmark contents.");
builder.endBookmark("MyBookmark");

let firstParagraphNodes = doc.firstSection.body.firstParagraph.getChildNodes(aw.NodeType.Any, false);

expect(firstParagraphNodes.at(0).nodeType).toEqual(aw.NodeType.BookmarkStart);
expect(firstParagraphNodes.at(1).nodeType).toEqual(aw.NodeType.Run);
expect(firstParagraphNodes.at(1).getText().trim()).toEqual("Bookmark contents.");
expect(firstParagraphNodes.at(2).nodeType).toEqual(aw.NodeType.BookmarkEnd);

// The document builder's cursor is always ahead of the node that we last added with it.
// If the builder's cursor is at the end of the document, its current node will be null.
// The previous node is the bookmark end node that we last added.
// Adding new nodes with the builder will append them to the last node.
expect(builder.currentNode).toBe(null);

// If we wish to edit a different part of the document with the builder,
// we will need to bring its cursor to the node we wish to edit.
builder.moveToBookmark("MyBookmark");

// Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
expect(builder.currentNode.referenceEquals(firstParagraphNodes.at(1))).toBe(true);

// We can also move the cursor to an individual node like this.
builder.moveTo(doc.firstSection.body.firstParagraph.getChildNodes(aw.NodeType.Any, false).at(0));

expect(builder.currentNode.nodeType).toEqual(aw.NodeType.BookmarkStart);
expect(builder.currentParagraph).toEqual(doc.firstSection.body.firstParagraph);
expect(builder.isAtStartOfParagraph).toEqual(true);

// We can use specific methods to move to the start/end of a document.
builder.moveToDocumentEnd();

expect(builder.isAtEndOfParagraph).toEqual(true);

builder.moveToDocumentStart();

expect(builder.isAtStartOfParagraph).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)
* property [DocumentBuilder.currentParagraph](../currentParagraph/)
* property [DocumentBuilder.currentStructuredDocumentTag](../currentStructuredDocumentTag/)

