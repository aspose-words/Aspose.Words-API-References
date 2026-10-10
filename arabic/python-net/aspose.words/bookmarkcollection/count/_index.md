---
title: BookmarkCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "BookmarkCollection.count property. Returns the number of bookmarks in the collection."
type: docs
weight: 20
url: /ar/python-net/aspose.words/bookmarkcollection/count/
---

## BookmarkCollection.count property

Returns the number of bookmarks in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to remove bookmarks from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج خمس إشارات مرجعية مع نص داخل حدودها.
i = 1
while i <= 5:
    bookmark_name = 'MyBookmark_' + str(i)
    builder.start_bookmark(bookmark_name)
    builder.write(f'Text inside {bookmark_name}.')
    builder.end_bookmark(bookmark_name)
    builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
    i += 1
# هذه المجموعة تخزن الإشارات المرجعية.
bookmarks = doc.range.bookmarks
self.assertEqual(5, bookmarks.count)
# هناك عدة طرق لإزالة الإشارات المرجعية.
# 1 -  استدعاء طريقة Remove للإشارة المرجعية:
bookmarks.get_by_name('MyBookmark_1').remove()
self.assertFalse(any([b.name == 'MyBookmark_1' for b in bookmarks]))
# 2 -  تمرير الإشارة المرجعية إلى طريقة Remove للمجموعة:
bookmark = doc.range.bookmarks[0]
doc.range.bookmarks.remove(bookmark=bookmark)
self.assertFalse(any([b.name == 'MyBookmark_2' for b in bookmarks]))
# 3 -  إزالة إشارة مرجعية من المجموعة بالاسم:
doc.range.bookmarks.remove(bookmark_name='MyBookmark_3')
self.assertFalse(any([b.name == 'MyBookmark_3' for b in bookmarks]))
# 4 -  إزالة إشارة مرجعية عند فهرس في مجموعة الإشارات المرجعية:
doc.range.bookmarks.remove_at(0)
self.assertFalse(any([b.name == 'MyBookmark_4' for b in bookmarks]))
# يمكننا مسح مجموعة الإشارات المرجعية بالكامل.
bookmarks.clear()
# النص الذي كان داخل الإشارات المرجعية لا يزال موجودًا في المستند.
self.assertEqual(0, bookmarks.count)
self.assertEqual('Text inside MyBookmark_1.\r' + 'Text inside MyBookmark_2.\r' + 'Text inside MyBookmark_3.\r' + 'Text inside MyBookmark_4.\r' + 'Text inside MyBookmark_5.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [BookmarkCollection](../)

