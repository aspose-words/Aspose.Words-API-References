---
title: Bookmark.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "Bookmark.remove method. Removes the bookmark from the document"
type: docs
weight: 80
url: /it/python-net/aspose.words/bookmark/remove/
---

## remove() {#default}

Removes the bookmark from the document. Does not remove text inside the bookmark.


```python
def remove(self):
    ...
```

### Examples

Shows how to remove bookmarks from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci cinque segnalibri con testo all'interno dei loro confini.
i = 1
while i <= 5:
    bookmark_name = 'MyBookmark_' + str(i)
    builder.start_bookmark(bookmark_name)
    builder.write(f'Text inside {bookmark_name}.')
    builder.end_bookmark(bookmark_name)
    builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
    i += 1
# Questa collezione memorizza i segnalibri.
bookmarks = doc.range.bookmarks
self.assertEqual(5, bookmarks.count)
# Esistono diversi modi per rimuovere i segnalibri.
# 1 -  Chiamare il metodo Remove del segnalibro:
bookmarks.get_by_name('MyBookmark_1').remove()
self.assertFalse(any([b.name == 'MyBookmark_1' for b in bookmarks]))
# 2 -  Passare il segnalibro al metodo Remove della collezione:
bookmark = doc.range.bookmarks[0]
doc.range.bookmarks.remove(bookmark=bookmark)
self.assertFalse(any([b.name == 'MyBookmark_2' for b in bookmarks]))
# 3 -  Rimuovere un segnalibro dalla collezione per nome:
doc.range.bookmarks.remove(bookmark_name='MyBookmark_3')
self.assertFalse(any([b.name == 'MyBookmark_3' for b in bookmarks]))
# 4 -  Rimuovere un segnalibro a un indice nella collezione dei segnalibri:
doc.range.bookmarks.remove_at(0)
self.assertFalse(any([b.name == 'MyBookmark_4' for b in bookmarks]))
# Possiamo svuotare l'intera collezione di segnalibri.
bookmarks.clear()
# Il testo che era all'interno dei segnalibri è ancora presente nel documento.
self.assertEqual(0, bookmarks.count)
self.assertEqual('Text inside MyBookmark_1.\r' + 'Text inside MyBookmark_2.\r' + 'Text inside MyBookmark_3.\r' + 'Text inside MyBookmark_4.\r' + 'Text inside MyBookmark_5.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

