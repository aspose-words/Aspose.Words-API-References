---
title: OutlineOptions.bookmarks_outline_levels property
linktitle: bookmarks_outline_levels property
articleTitle: bookmarks_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.bookmarks_outline_levels property. Allows to specify individual bookmarks outline level."
type: docs
weight: 20
url: /ru/python-net/aspose.words.saving/outlineoptions/bookmarks_outline_levels/
---

## OutlineOptions.bookmarks_outline_levels property

Allows to specify individual bookmarks outline level.


```python
@property
def bookmarks_outline_levels(self) -> aspose.words.saving.BookmarksOutlineLevelCollection:
    ...

```

### Remarks

If bookmark level is not specified in this collection then [OutlineOptions.default_bookmarks_outline_level](../default_bookmarks_outline_level/) value is used.




### Examples

Shows how to set outline levels for bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте закладку, внутри которой вложена другая закладка.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# Вставьте другую закладку.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# При сохранении в .pdf закладки можно открыть через выпадающее меню и использовать в качестве якорей большинством читалок.
# У закладок также могут быть числовые значения уровней оглавления,
# что позволяет записям нижнего уровня скрывать дочерние записи более высокого уровня при свертывании в читалке.
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
# Мы можем удалить два элемента, оставив только обозначение уровня оглавления для "Bookmark 1".
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# Существует девять уровней оглавления. Их нумерация будет оптимизирована во время операции сохранения.
# В этом случае уровни "5" и "9" станут "2" и "3".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# Очистка этой коллекции сохранит закладки и разместит их все на одном уровне оглавления.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

