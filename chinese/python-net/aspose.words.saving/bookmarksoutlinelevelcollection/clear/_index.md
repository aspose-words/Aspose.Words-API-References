---
title: BookmarksOutlineLevelCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "BookmarksOutlineLevelCollection.clear method. Removes all elements from the collection."
type: docs
weight: 50
url: /zh/python-net/aspose.words.saving/bookmarksoutlinelevelcollection/clear/
---

## clear() {#default}

Removes all elements from the collection.


```python
def clear(self):
    ...
```

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

* module [aspose.words.saving](../../)
* class [BookmarksOutlineLevelCollection](../)

