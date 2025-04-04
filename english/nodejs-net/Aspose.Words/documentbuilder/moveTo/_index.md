---
title: DocumentBuilder.moveTo method
linktitle: moveTo method
articleTitle: moveTo method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.moveTo method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /nodejs-net/aspose.words/documentbuilder/moveTo/
---

## moveTo(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```js
moveTo(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Run 1. ");

// The document builder has a cursor, which acts as the part of the document
// where the builder appends new nodes when we use its document construction methods.
// This cursor functions in the same way as Microsoft Word's blinking cursor,
// and it also always ends up immediately after any node that the builder just inserted.
// To append content to a different part of the document,
// we can move the cursor to a different node with the "MoveTo" method.
expect(builder.currentParagraph).toEqual(doc.firstSection.body.lastParagraph);
builder.moveTo(doc.firstSection.body.firstParagraph.runs.at(0));
expect(builder.currentParagraph).toEqual(doc.firstSection.body.firstParagraph);

// The cursor is now in front of the node that we moved it to.
// Adding a second run will insert it in front of the first run.
builder.writeln("Run 2. ");

expect(doc.getText().trim()).toEqual("Run 2. \rRun 1.");

// Move the cursor to the end of the document to continue appending text to the end as before.
builder.moveTo(doc.lastSection.body.lastParagraph);
builder.writeln("Run 3. ");

expect(doc.getText().trim()).toEqual("Run 2. \rRun 1. \rRun 3.");
expect(builder.currentParagraph).toEqual(doc.firstSection.body.lastParagraph);
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

