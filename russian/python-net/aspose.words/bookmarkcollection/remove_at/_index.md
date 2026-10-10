---
title: BookmarkCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "BookmarkCollection.remove_at method. Removes a bookmark at the specified index."
type: docs
weight: 60
url: /ru/python-net/aspose.words/bookmarkcollection/remove_at/
---

## remove_at(index) {#int}

Removes a bookmark at the specified index.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the bookmark to remove. |

### Examples

Shows how to remove bookmarks from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте пять закладок с текстом внутри их границ.
i = 1
while i <= 5:
    bookmark_name = 'MyBookmark_' + str(i)
    builder.start_bookmark(bookmark_name)
    builder.write(f'Text inside {bookmark_name}.')
    builder.end_bookmark(bookmark_name)
    builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
    i += 1
# Эта коллекция хранит закладки.
bookmarks = doc.range.bookmarks
self.assertEqual(5, bookmarks.count)
# Существует несколько способов удаления закладок.
# 1 -  Вызов метода Remove у закладки:
bookmarks.get_by_name('MyBookmark_1').remove()
self.assertFalse(any([b.name == 'MyBookmark_1' for b in bookmarks]))
# 2 -  Передача закладки в метод Remove коллекции:
bookmark = doc.range.bookmarks[0]
doc.range.bookmarks.remove(bookmark=bookmark)
self.assertFalse(any([b.name == 'MyBookmark_2' for b in bookmarks]))
# 3 -  Удаление закладки из коллекции по имени:
doc.range.bookmarks.remove(bookmark_name='MyBookmark_3')
self.assertFalse(any([b.name == 'MyBookmark_3' for b in bookmarks]))
# 4 -  Удаление закладки по индексу в коллекции закладок:
doc.range.bookmarks.remove_at(0)
self.assertFalse(any([b.name == 'MyBookmark_4' for b in bookmarks]))
# Мы можем очистить всю коллекцию закладок.
bookmarks.clear()
# Текст, который был внутри закладок, всё ещё присутствует в документе.
self.assertEqual(0, bookmarks.count)
self.assertEqual('Text inside MyBookmark_1.\r' + 'Text inside MyBookmark_2.\r' + 'Text inside MyBookmark_3.\r' + 'Text inside MyBookmark_4.\r' + 'Text inside MyBookmark_5.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [BookmarkCollection](../)

