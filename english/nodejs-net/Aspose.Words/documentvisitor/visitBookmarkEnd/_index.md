---
title: DocumentVisitor.visitBookmarkEnd method
linktitle: visitBookmarkEnd method
articleTitle: visitBookmarkEnd method
second_title: Aspose.Words for Node.js
description: "DocumentVisitor.visitBookmarkEnd method. Called when an end of a bookmark is encountered in the document."
type: docs
weight: 40
url: /nodejs-net/aspose.words/documentvisitor/visitBookmarkEnd/
---

## visitBookmarkEnd(bookmarkEnd) {#bookmarkend}

Called when an end of a bookmark is encountered in the document.


```js
visitBookmarkEnd(bookmarkEnd: Aspose.Words.BookmarkEnd)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkEnd | [BookmarkEnd](../../bookmarkend/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


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
* class [DocumentVisitor](../)

