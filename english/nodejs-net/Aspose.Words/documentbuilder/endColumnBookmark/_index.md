---
title: DocumentBuilder.endColumnBookmark method
linktitle: endColumnBookmark method
articleTitle: endColumnBookmark method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.endColumnBookmark method. Marks the current position in the document as a column bookmark end"
type: docs
weight: 220
url: /nodejs-net/Aspose.Words/documentbuilder/endColumnBookmark/
---

## endColumnBookmark(bookmarkName) {#string}

Marks the current position in the document as a column bookmark end. The position must be in a table cell.


```js
endColumnBookmark(bookmarkName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | string | Name of the bookmark. |

### Remarks

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you
need to call both [DocumentBuilder.startColumnBookmark()](../startColumnBookmark/#string) and [DocumentBuilder.endColumnBookmark()](./#string) with the same
*bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkEnd](../../bookmarkend/) node may differ from the current document
builder position.




### Returns

The bookmark end node that was just created.


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

