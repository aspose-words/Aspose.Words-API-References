---
title: BookmarksOutlineLevelCollection indexer
linktitle: BookmarksOutlineLevelCollection indexer
articleTitle: BookmarksOutlineLevelCollection indexer
second_title: Aspose.Words for Python
description: "BookmarksOutlineLevelCollection indexer. Gets or sets a bookmark outline level at the specified index."
type: docs
weight: 20
url: /it/python-net/aspose.words.saving/bookmarksoutlinelevelcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets a bookmark outline level at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Returns

The outline level of the bookmark. Valid range is 0 to 9.


### Examples

Shows how to set outline levels for bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un segnalibro con un altro segnalibro annidato al suo interno.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# Inserisci un altro segnalibro.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# Durante il salvataggio in .pdf, i segnalibri possono essere accessibili tramite un menu a discesa e usati come ancore dalla maggior parte dei lettori.
# I segnalibri possono anche avere valori numerici per i livelli di contorno,
# consentendo alle voci di contorno di livello inferiore di nascondere le voci figlio di livello superiore quando vengono compresse nel lettore.
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
# Possiamo rimuovere due elementi in modo che rimanga solo la designazione del livello di contorno per "Bookmark 1".
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# Ci sono nove livelli di contorno. La loro numerazione sarà ottimizzata durante l'operazione di salvataggio.
# In questo caso, i livelli "5" e "9" diventeranno "2" e "3".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# Svuotare questa collezione preserverà i segnalibri e li posizionerà tutti sullo stesso livello di contorno.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../../)
* class [BookmarksOutlineLevelCollection](../)

