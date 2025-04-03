---
title: DocumentBuilder.endBookmark method
linktitle: endBookmark method
articleTitle: endBookmark method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.endBookmark method. Marks the current position in the document as a bookmark end."
type: docs
weight: 210
url: /nodejs-net/aspose.words/documentbuilder/endBookmark/
---

## endBookmark(bookmarkName) {#string}

Marks the current position in the document as a bookmark end.


```js
endBookmark(bookmarkName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | string | Name of the bookmark. |

### Remarks

Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to
call both [DocumentBuilder.startBookmark()](../startBookmark/#string) and [DocumentBuilder.endBookmark()](./#string) with the same *bookmarkName*
parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.




### Returns

The bookmark end node that was just created.


### Examples

Shows how create a bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A valid bookmark needs to have document body text enclosed by
// BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
builder.startBookmark("MyBookmark");
builder.writeln("Hello world!");
builder.endBookmark("MyBookmark");

expect(doc.range.bookmarks.count).toEqual(1);
expect(doc.range.bookmarks.at(0).name).toEqual("MyBookmark");
expect(doc.range.bookmarks.at(0).text.trim()).toEqual("Hello world!");
```

Shows how to insert a hyperlink which references a local bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startBookmark("Bookmark1");
builder.write("Bookmarked text. ");
builder.endBookmark("Bookmark1");
builder.writeln("Text outside of the bookmark.");

// Insert a HYPERLINK field that links to the bookmark. We can pass field switches
// to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
builder.font.color = "#0000FF";
builder.font.underline = aw.Underline.Single;
let hyperlink = builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true).asFieldHyperlink();
hyperlink.screenTip = "Hyperlink Tip";

doc.save(base.artifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

