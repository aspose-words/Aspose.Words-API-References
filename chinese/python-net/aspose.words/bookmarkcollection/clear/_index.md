---
title: BookmarkCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "BookmarkCollection.clear method. Removes all bookmarks from this collection and from the document."
type: docs
weight: 30
url: /zh/python-net/aspose.words/bookmarkcollection/clear/
---

## clear() {#default}

Removes all bookmarks from this collection and from the document.


```python
def clear(self):
    ...
```

### Examples

Shows how to remove bookmarks from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入五个书签，并在其边界内放置文本。
i = 1
while i <= 5:
    bookmark_name = 'MyBookmark_' + str(i)
    builder.start_bookmark(bookmark_name)
    builder.write(f'Text inside {bookmark_name}.')
    builder.end_bookmark(bookmark_name)
    builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
    i += 1
# 此集合存储书签。
bookmarks = doc.range.bookmarks
self.assertEqual(5, bookmarks.count)
# 有多种删除书签的方法。
# 1 -  调用书签的 Remove 方法:
bookmarks.get_by_name('MyBookmark_1').remove()
self.assertFalse(any([b.name == 'MyBookmark_1' for b in bookmarks]))
# 2 -  将书签传递给集合的 Remove 方法:
bookmark = doc.range.bookmarks[0]
doc.range.bookmarks.remove(bookmark=bookmark)
self.assertFalse(any([b.name == 'MyBookmark_2' for b in bookmarks]))
# 3 -  通过名称从集合中删除书签:
doc.range.bookmarks.remove(bookmark_name='MyBookmark_3')
self.assertFalse(any([b.name == 'MyBookmark_3' for b in bookmarks]))
# 4 -  在书签集合中按索引删除书签:
doc.range.bookmarks.remove_at(0)
self.assertFalse(any([b.name == 'MyBookmark_4' for b in bookmarks]))
# 我们可以清除整个书签集合。
bookmarks.clear()
# 书签内部的文本仍然存在于文档中。
self.assertEqual(0, bookmarks.count)
self.assertEqual('Text inside MyBookmark_1.\r' + 'Text inside MyBookmark_2.\r' + 'Text inside MyBookmark_3.\r' + 'Text inside MyBookmark_4.\r' + 'Text inside MyBookmark_5.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [BookmarkCollection](../)

