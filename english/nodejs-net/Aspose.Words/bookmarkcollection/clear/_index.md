---
title: BookmarkCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for NodeJs
description: "BookmarkCollection.clear method. Removes all bookmarks from this collection and from the document."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/bookmarkcollection/clear/
---

## clear() {#default}

Removes all bookmarks from this collection and from the document.


```js
clear()
```

### Examples

Shows how to remove bookmarks from a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert five bookmarks with text inside their boundaries.
for (let i = 1; i <= 5; i++)
{
  let bookmarkName = "MyBookmark_" + i;

  builder.startBookmark(bookmarkName);
  builder.write(`Text inside ${bookmarkName}.`);
  builder.endBookmark(bookmarkName);
  builder.insertBreak(aw.BreakType.ParagraphBreak);
}

// This collection stores bookmarks.
let bookmarks = doc.range.bookmarks;

expect(bookmarks.count).toEqual(5);

// There are several ways of removing bookmarks.
// 1 -  Calling the bookmark's Remove method:
bookmarks.at("MyBookmark_1").remove();

for (let b of bookmarks)
  expect(b.Name).not.toEqual("MyBookmark_1");

// 2 -  Passing the bookmark to the collection's Remove method:
let bookmark = doc.range.bookmarks.at(0);
doc.range.bookmarks.remove(bookmark);

for (let b of bookmarks)
  expect(b.Name).not.toEqual("MyBookmark_2");

// 3 -  Removing a bookmark from the collection by name:
doc.range.bookmarks.remove("MyBookmark_3");

for (let b of bookmarks)
  expect(b.Name).not.toEqual("MyBookmark_3");

// 4 -  Removing a bookmark at an index in the bookmark collection:
doc.range.bookmarks.removeAt(0);

for (let b of bookmarks)
  expect(b.Name).not.toEqual("MyBookmark_4");

// We can clear the entire bookmark collection.
bookmarks.clear();

// The text that was inside the bookmarks is still present in the document.
expect(bookmarks.count).toEqual(0);
expect(doc.getText().trim()).toEqual("Text inside MyBookmark_1.\r" +
        "Text inside MyBookmark_2.\r" +
        "Text inside MyBookmark_3.\r" +
        "Text inside MyBookmark_4.\r" +
        "Text inside MyBookmark_5.");
```

### See Also

* module [Aspose.Words](../../)
* class [BookmarkCollection](../)

