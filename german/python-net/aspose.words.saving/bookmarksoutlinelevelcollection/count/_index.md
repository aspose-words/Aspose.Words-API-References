---
title: BookmarksOutlineLevelCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "BookmarksOutlineLevelCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/bookmarksoutlinelevelcollection/count/
---

## BookmarksOutlineLevelCollection.count property

Gets the number of elements contained in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to set outline levels for bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein Lesezeichen ein, das ein weiteres Lesezeichen verschachtelt enthält.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# Fügen Sie ein weiteres Lesezeichen ein.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# Beim Speichern als .pdf können Lesezeichen über ein Dropdown‑Menü aufgerufen und von den meisten Lesern als Anker verwendet werden.
# Lesezeichen können außerdem numerische Werte für Gliederungsebenen haben,
# was es ermöglicht, dass Einträge niedrigerer Ebenen höhere Kind‑Einträge ausblenden, wenn sie im Leser zusammengeklappt sind.
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
# Wir können zwei Elemente entfernen, sodass nur die Gliederungsebene‑Bezeichnung für \"Bookmark 1\" übrig bleibt.
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# Es gibt neun Gliederungsebenen. Ihre Nummerierung wird während des Speichervorgangs optimiert.
# In diesem Fall werden die Ebenen \"5\" und \"9\" zu \"2\" bzw. \"3\".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# Das Leeren dieser Sammlung bewahrt die Lesezeichen und legt sie alle auf dieselbe Gliederungsebene.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../../)
* class [BookmarksOutlineLevelCollection](../)

