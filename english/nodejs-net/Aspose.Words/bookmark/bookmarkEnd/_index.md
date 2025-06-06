﻿---
title: Bookmark.bookmarkEnd property
linktitle: bookmarkEnd property
articleTitle: bookmarkEnd property
second_title: Aspose.Words for Node.js
description: "Bookmark.bookmarkEnd property. Gets the node that represents the end of the bookmark."
type: docs
weight: 10
url: /nodejs-net/aspose.words/bookmark/bookmarkEnd/
---

## Bookmark.bookmarkEnd property

Gets the node that represents the end of the bookmark.


```js
get bookmarkEnd(): Aspose.Words.BookmarkEnd
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
* class [Bookmark](../)

