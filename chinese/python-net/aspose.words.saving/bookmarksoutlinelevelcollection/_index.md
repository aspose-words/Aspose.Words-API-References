---
title: BookmarksOutlineLevelCollection class
linktitle: BookmarksOutlineLevelCollection class
articleTitle: BookmarksOutlineLevelCollection class
second_title: Aspose.Words for Python
description: "aspose.words.saving.BookmarksOutlineLevelCollection class. A collection of individual bookmarks outline level"
type: docs
weight: 10
url: /zh/python-net/aspose.words.saving/bookmarksoutlinelevelcollection/
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
# 插入一个书签，并在其内部嵌套另一个书签。
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# 插入另一个书签。
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# 保存为 .pdf 时，书签可以通过下拉菜单访问，并被大多数阅读器用作锚点。
# 书签还可以为大纲级别设置数值，
# 在阅读器中折叠时，使低级别的大纲条目隐藏高级别的子条目。
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
# 我们可以删除两个元素，只保留 "Bookmark 1" 的大纲级别标识。
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# 共有九个大纲级别。它们的编号将在保存操作期间进行优化。
# 在这种情况下，级别 "5" 和 "9" 将变为 "2" 和 "3"。
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# 清空此集合将保留书签，并将它们全部放在同一级别的大纲中。
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../)

