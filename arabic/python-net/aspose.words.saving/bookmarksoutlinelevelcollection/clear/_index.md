---
title: BookmarksOutlineLevelCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "BookmarksOutlineLevelCollection.clear method. Removes all elements from the collection."
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/bookmarksoutlinelevelcollection/clear/
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
# إدراج إشارة مرجعية مع إشارة مرجعية أخرى متداخلة داخلها.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# إدراج إشارة مرجعية أخرى.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# عند الحفظ إلى .pdf، يمكن الوصول إلى الإشارات المرجعية عبر قائمة منسدلة واستخدامها كمرساة في معظم القارئات.
# يمكن للإشارات المرجعية أيضًا أن تحتوي على قيم رقمية لمستويات المخطط،
# مما يسمح للمدخلات ذات المستوى الأدنى إخفاء المدخلات الفرعية ذات المستوى الأعلى عند طيها في القارئ.
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
# يمكننا إزالة عنصرين بحيث يبقى فقط تعيين مستوى المخطط لـ "Bookmark 1".
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# هناك تسعة مستويات مخطط. سيتم تحسين ترقيمها أثناء عملية الحفظ.
# في هذه الحالة، المستويات "5" و "9" ستصبح "2" و "3".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# إفراغ هذه المجموعة سيحافظ على الإشارات المرجعية ويضعها جميعًا على نفس مستوى المخطط.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../../)
* class [BookmarksOutlineLevelCollection](../)

