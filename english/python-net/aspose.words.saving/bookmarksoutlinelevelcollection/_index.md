---
title: BookmarksOutlineLevelCollection class
linktitle: BookmarksOutlineLevelCollection class
articleTitle: BookmarksOutlineLevelCollection class
second_title: Aspose.Words for Python
description: "aspose.words.saving.BookmarksOutlineLevelCollection class. A collection of individual bookmarks outline level"
type: docs
weight: 10
url: /python-net/aspose.words.saving/bookmarksoutlinelevelcollection/
---

## BookmarksOutlineLevelCollection class

A collection of individual bookmarks outline level.
To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/python-net/working-with-bookmarks/) documentation article.




### Remarks

Key is a case-insensitive string bookmark name. Value is a int bookmark outline level.

Bookmark outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline.
Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.




### Constructors
| Name | Description |
| --- | --- |
| [BookmarksOutlineLevelCollection()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets a bookmark outline level at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(name, outline_level)](./add/#str_int) | Adds a bookmark to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ contains(name)](./contains/#str) | Determines whether the collection contains a bookmark with the given name. |
|[ get_by_name(name)](./get_by_name/#str) | Gets or a sets a bookmark outline level by the bookmark name. |
|[ index_of_key(name)](./index_of_key/#str) | Returns the zero-based index of the specified bookmark in the collection. |
|[ remove(name)](./remove/#str) | Removes a bookmark with the specified name from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a bookmark at the specified index. |

### Examples

Shows how to set outline levels for bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a bookmark with another bookmark nested inside it.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# Insert another bookmark.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
# Bookmarks can also have numeric values for outline levels,
# enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
pdf_save_options = aw.saving.PdfSaveOptions()
outline_levels = pdf_save_options.outline_options.bookmarks_outline_levels
outline_levels.add('Bookmark 1', 1)
outline_levels.add('Bookmark 2', 2)
outline_levels.add('Bookmark 3', 3)
self.assertEqual(3, outline_levels.count)
self.assertTrue(outline_levels.contains('Bookmark 1'))
self.assertEqual(1, outline_levels[0])
self.assertEqual(2, outline_levels.get_by_name('Bookmark 2'))
self.assertEqual(2, outline_levels.index_of_key('Bookmark 3'))
# We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# There are nine outline levels. Their numbering will be optimized during the save operation.
# In this case, levels "5" and "9" will become "2" and "3".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# Emptying this collection will preserve the bookmarks and put them all on the same outline level.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../)

