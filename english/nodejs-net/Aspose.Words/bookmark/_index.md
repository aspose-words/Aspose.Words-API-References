---
title: Bookmark class
linktitle: Bookmark class
articleTitle: Bookmark class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Bookmark class. Represents a single bookmark"
type: docs
weight: 60
url: /nodejs-net/aspose.words/bookmark/
---

## Bookmark class

Represents a single bookmark.
To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/nodejs-net/working-with-bookmarks/) documentation article.




### Remarks

[Bookmark](./) is a "facade" object that encapsulates two nodes [Bookmark.bookmarkStart](./bookmarkStart/)
and [Bookmark.bookmarkEnd](./bookmarkEnd/) in a document tree and allows to work with a bookmark as a single object.




### Properties

| Name | Description |
| --- | --- |
| [bookmarkEnd](./bookmarkEnd/) | Gets the node that represents the end of the bookmark. |
| [bookmarkStart](./bookmarkStart/) | Gets the node that represents the start of the bookmark. |
| [firstColumn](./firstColumn/) | Gets the zero-based index of the first column of the table column range associated with the bookmark. |
| [isColumn](./isColumn/) | Returns ``true`` if this bookmark is a table column bookmark. |
| [lastColumn](./lastColumn/) | Gets the zero-based index of the last column of the table column range associated with the bookmark. |
| [name](./name/) | Gets or sets the name of the bookmark. |
| [text](./text/) | Gets or sets the text enclosed in the bookmark. |

### Methods

| Name | Description |
| --- | --- |
|[ remove()](./remove/#default) | Removes the bookmark from the document. Does not remove text inside the bookmark. |

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

