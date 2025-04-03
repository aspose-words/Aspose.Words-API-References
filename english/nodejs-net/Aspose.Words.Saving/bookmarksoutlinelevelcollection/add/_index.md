---
title: BookmarksOutlineLevelCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for NodeJs
description: "BookmarksOutlineLevelCollection.add method. Adds a bookmark to the collection."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/bookmarksoutlinelevelcollection/add/
---

## add(name, outlineLevel) {#string_number}

Adds a bookmark to the collection.


```js
add(name: stringoutlineLevel: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The case-insensitive name of the bookmark to add. |
| outlineLevel | number | The outline level of the bookmark. Valid range is 0 to 9. |

### Examples

Shows how to set outline levels for bookmarks.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a bookmark with another bookmark nested inside it.
builder.startBookmark("Bookmark 1");
builder.writeln("Text inside Bookmark 1.");

builder.startBookmark("Bookmark 2");
builder.writeln("Text inside Bookmark 1 and 2.");
builder.endBookmark("Bookmark 2");

builder.writeln("Text inside Bookmark 1.");
builder.endBookmark("Bookmark 1");

// Insert another bookmark.
builder.startBookmark("Bookmark 3");
builder.writeln("Text inside Bookmark 3.");
builder.endBookmark("Bookmark 3");

// When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
// Bookmarks can also have numeric values for outline levels,
// enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
let pdfSaveOptions = new aw.Saving.PdfSaveOptions();
let outlineLevels = pdfSaveOptions.outlineOptions.bookmarksOutlineLevels;

outlineLevels.add("Bookmark 1", 1);
outlineLevels.add("Bookmark 2", 2);
outlineLevels.add("Bookmark 3", 3);

expect(outlineLevels.count).toEqual(3);
expect(outlineLevels.contains("Bookmark 1")).toEqual(true);
expect(outlineLevels.at(0)).toEqual(1);
expect(outlineLevels.at("Bookmark 2")).toEqual(2);
expect(outlineLevels.indexOfKey("Bookmark 3")).toEqual(2);

// We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
outlineLevels.removeAt(2);
outlineLevels.remove("Bookmark 2");

// There are nine outline levels. Their numbering will be optimized during the save operation.
// In this case, levels "5" and "9" will become "2" and "3".
outlineLevels.add("Bookmark 2", 5);
outlineLevels.add("Bookmark 3", 9);

doc.save(base.artifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Emptying this collection will preserve the bookmarks and put them all on the same outline level.
outlineLevels.clear();
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [BookmarksOutlineLevelCollection](../)

