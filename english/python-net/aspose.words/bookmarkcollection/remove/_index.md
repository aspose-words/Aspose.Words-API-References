---
title: BookmarkCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "aspose.words.BookmarkCollection.remove method"
type: docs
weight: 50
url: /python-net/aspose.words/bookmarkcollection/remove/
---

## remove(bookmark) {#bookmark}

Removes the specified bookmark from the document.


```python
def remove(self, bookmark: aspose.words.Bookmark):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark | [Bookmark](../../bookmark/) | The bookmark to remove. |

## remove(bookmark_name) {#str}

Removes a bookmark with the specified name.


```python
def remove(self, bookmark_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | The case-insensitive name of the bookmark to remove. |

## Examples

Shows how to remove bookmarks from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert five bookmarks with text inside their boundaries.
i = 1
while i <= 5:
    bookmark_name = 'MyBookmark_' + str(i)
    builder.start_bookmark(bookmark_name)
    builder.write(f'Text inside {bookmark_name}.')
    builder.end_bookmark(bookmark_name)
    builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
    i += 1
# This collection stores bookmarks.
bookmarks = doc.range.bookmarks
self.assertEqual(5, bookmarks.count)
# There are several ways of removing bookmarks.
# 1 -  Calling the bookmark's Remove method:
bookmarks.get_by_name('MyBookmark_1').remove()
self.assertFalse(any([b.name == 'MyBookmark_1' for b in bookmarks]))
# 2 -  Passing the bookmark to the collection's Remove method:
bookmark = doc.range.bookmarks[0]
doc.range.bookmarks.remove(bookmark=bookmark)
self.assertFalse(any([b.name == 'MyBookmark_2' for b in bookmarks]))
# 3 -  Removing a bookmark from the collection by name:
doc.range.bookmarks.remove(bookmark_name='MyBookmark_3')
self.assertFalse(any([b.name == 'MyBookmark_3' for b in bookmarks]))
# 4 -  Removing a bookmark at an index in the bookmark collection:
doc.range.bookmarks.remove_at(0)
self.assertFalse(any([b.name == 'MyBookmark_4' for b in bookmarks]))
# We can clear the entire bookmark collection.
bookmarks.clear()
# The text that was inside the bookmarks is still present in the document.
self.assertEqual(0, bookmarks.count)
self.assertEqual('Text inside MyBookmark_1.\r' + 'Text inside MyBookmark_2.\r' + 'Text inside MyBookmark_3.\r' + 'Text inside MyBookmark_4.\r' + 'Text inside MyBookmark_5.', doc.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [BookmarkCollection](../)

