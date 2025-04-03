---
title: DocumentBuilder.moveToBookmark method
linktitle: moveToBookmark method
articleTitle: moveToBookmark method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.moveToBookmark method"
type: docs
weight: 530
url: /nodejs-net/aspose.words/documentbuilder/moveToBookmark/
---

## moveToBookmark(bookmarkName) {#string}

Moves the cursor to a bookmark.


```js
moveToBookmark(bookmarkName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | string | The name of the bookmark to move the cursor to. |

### Remarks

Moves the cursor to a position just after the start of the bookmark with the
specified name.

The comparison is not case-sensitive. If the bookmark was not found, ``false`` is
returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields.
Moving to such a bookmark and inserting text there inserts the text into the
form field code. Although this will not invalidate the form field, the inserted
text will not be visible because it becomes part of the field code.




### Returns

``true`` if the bookmark was found; ``false`` otherwise.


## moveToBookmark(bookmarkName, isStart, isAfter) {#string_boolean_boolean}

Moves the cursor to a bookmark with greater precision.


```js
moveToBookmark(bookmarkName: string, isStart: boolean, isAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | string | The name of the bookmark to move the cursor to. |
| isStart | boolean | When ``true``, moves the cursor to the beginning of the bookmark. When ``false``, moves the cursor to the end of the bookmark. |
| isAfter | boolean | When ``true``, moves the cursor to be after the bookmark start or end position. When ``false``, moves the cursor to be before the bookmark start or end position. |

### Remarks

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, ``false`` is
returned and the cursor is not moved.




### Returns

``true`` if the bookmark was found; ``false`` otherwise.


## Examples

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

Shows how to move a document builder's node insertion point cursor to a bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
// matching bookmark name somewhere afterward, and contents enclosed by those nodes.
builder.startBookmark("MyBookmark");
builder.write("Hello world! ");
builder.endBookmark("MyBookmark");

// There are 4 ways of moving a document builder's cursor to a bookmark.
// If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
// This means that any text added by the builder will become a part of the bookmark.
// 1 -  Outside of the bookmark, in front of the BookmarkStart node:
expect(builder.moveToBookmark("MyBookmark", true, false)).toEqual(true);
builder.write("1. ");

expect(doc.range.bookmarks.at("MyBookmark").text).toEqual("Hello world! ");
expect(doc.getText().trim()).toEqual("1. Hello world!");

// 2 -  Inside the bookmark, right after the BookmarkStart node:
expect(builder.moveToBookmark("MyBookmark", true, true)).toEqual(true);
builder.write("2. ");

expect(doc.range.bookmarks.at("MyBookmark").text).toEqual("2. Hello world! ");
expect(doc.getText().trim()).toEqual("1. 2. Hello world!");

// 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
expect(builder.moveToBookmark("MyBookmark", false, false)).toEqual(true);
builder.write("3. ");

expect(doc.range.bookmarks.at("MyBookmark").text).toEqual("2. Hello world! 3. ");
expect(doc.getText().trim()).toEqual("1. 2. Hello world! 3.");

// 4 -  Outside of the bookmark, after the BookmarkEnd node:
expect(builder.moveToBookmark("MyBookmark", false, true)).toEqual(true);
builder.write("4.");

expect(doc.range.bookmarks.at("MyBookmark").text).toEqual("2. Hello world! 3. ");
expect(doc.getText().trim()).toEqual("1. 2. Hello world! 3. 4.");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

