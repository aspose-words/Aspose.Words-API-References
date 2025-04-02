---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/bookmark/name/
---

## Bookmark.name property

Gets or sets the name of the bookmark.


```js
get name(): string
```

### Remarks

Note that if you change the name of a bookmark to a name that already exists in the document,
no error will be given and only the first bookmark will be stored when you save the document.


### Examples

Shows how to insert a bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A valid bookmark has a name, a BookmarkStart, and a BookmarkEnd node.
// Any whitespace in the names of bookmarks will be converted to underscores if we open the saved document with Microsoft Word. 
// If we highlight the bookmark's name in Microsoft Word via Insert -> Links -> Bookmark, and press "Go To",
// the cursor will jump to the text enclosed between the BookmarkStart and BookmarkEnd nodes.
builder.startBookmark("My Bookmark");
builder.write("Contents of MyBookmark.");
builder.endBookmark("My Bookmark");

// Bookmarks are stored in this collection.
expect(doc.range.bookmarks.at(0).name).toEqual("My Bookmark");

doc.save(base.artifactsDir + "Bookmarks.insert.docx");
```

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

