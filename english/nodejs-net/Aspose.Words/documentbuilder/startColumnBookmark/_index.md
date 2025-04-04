---
title: DocumentBuilder.startColumnBookmark method
linktitle: startColumnBookmark method
articleTitle: startColumnBookmark method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.startColumnBookmark method. Marks the current position in the document as a column bookmark start"
type: docs
weight: 660
url: /nodejs-net/aspose.words/documentbuilder/startColumnBookmark/
---

## startColumnBookmark(bookmarkName) {#string}

Marks the current position in the document as a column bookmark start. The position must be in a table cell.


```js
startColumnBookmark(bookmarkName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | string | Name of the bookmark. |

### Remarks

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you
need to call both [DocumentBuilder.startColumnBookmark()](./#string) and [DocumentBuilder.endColumnBookmark()](../endColumnBookmark/#string) with the same
*bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkStart](../../bookmarkstart/) node may differ from the current document
builder position.




### Returns

The bookmark start node that was just created.


### Examples

Shows how to create a column bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startTable();

builder.insertCell();
// Cells 1,2,4,5 will be bookmarked.
builder.startColumnBookmark("MyBookmark_1");
// Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
builder.startColumnBookmark("MyBookmark_1");
builder.startColumnBookmark("BadStartBookmark");
builder.write("Cell 1");

builder.insertCell();
builder.write("Cell 2");

builder.insertCell();
builder.write("Cell 3");

builder.endRow();

builder.insertCell();
builder.write("Cell 4");

builder.insertCell();
builder.write("Cell 5");
builder.endColumnBookmark("MyBookmark_1");
builder.endColumnBookmark("MyBookmark_1");

expect(() => builder.endColumnBookmark("BadEndBookmark")).toThrow("The corresponding bookmark start must be in the same table.");

builder.insertCell();
builder.write("Cell 6");

builder.endRow();
builder.endTable();

doc.save(base.artifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

