---
title: Range.bookmarks property
linktitle: bookmarks property
articleTitle: bookmarks property
second_title: Aspose.Words for NodeJs
description: "Range.bookmarks property. Returns a [Range.bookmarks](./) collection that represents all bookmarks in the range."
type: docs
weight: 10
url: /nodejs-net/aspose.words/range/bookmarks/
---

## Range.bookmarks property

Returns a [Range.bookmarks](./) collection that represents all bookmarks in the range.



```js
get bookmarks(): Aspose.Words.BookmarkCollection
```

### Examples

Shows how to add bookmarks and update their contents.

```js
test('CreateUpdateAndPrintBookmarks', () => {
  // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
  let doc = CreateDocumentWithBookmarks(3);
  let bookmarks = doc.range.bookmarks;
  expect(bookmarks.count).toEqual(3);

  // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
  bookmarks.at(0).name = `${bookmarks.at(0).name}_NewName`;
  bookmarks.at("MyBookmark_2").text = `Updated text contents of ${bookmarks.at(1).name}`;
});
```

### See Also

* module [Aspose.Words](../../)
* class [Range](../)

