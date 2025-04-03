---
title: BookmarkStart.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "BookmarkStart.name property. Gets or sets the bookmark name."
type: docs
weight: 30
url: /nodejs-net/aspose.words/bookmarkstart/name/
---

## BookmarkStart.name property

Gets or sets the bookmark name.


```js
get name(): string
```

### Remarks

Cannot be ``null``.




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
* class [BookmarkStart](../)

