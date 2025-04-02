---
title: BookmarkCollection class
linktitle: BookmarkCollection class
articleTitle: BookmarkCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.BookmarkCollection class. A collection of [Bookmark](../bookmark/) objects that represent the bookmarks in the specified range"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/bookmarkcollection/
---

## BookmarkCollection class

A collection of [Bookmark](../bookmark/) objects that represent the bookmarks in the specified range.
To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/nodejs-net/working-with-bookmarks/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of bookmarks in the collection. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all bookmarks from this collection and from the document. |
|[ remove(bookmark)](./remove/#bookmark) | Removes the specified bookmark from the document. |
|[ remove(bookmarkName)](./remove/#string) | Removes a bookmark with the specified name. |
|[ removeAt(index)](./removeAt/#number) | Removes a bookmark at the specified index. |

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

* module [Aspose.Words](../)

