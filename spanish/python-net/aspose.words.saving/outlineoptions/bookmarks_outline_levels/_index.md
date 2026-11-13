---
title: OutlineOptions.bookmarks_outline_levels property
linktitle: bookmarks_outline_levels property
articleTitle: bookmarks_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.bookmarks_outline_levels property. Allows to specify individual bookmarks outline level."
type: docs
weight: 20
url: /es/python-net/aspose.words.saving/outlineoptions/bookmarks_outline_levels/
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
# Inserte un marcador con otro marcador anidado dentro de él.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# Inserte otro marcador.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# Al guardar en .pdf, los marcadores pueden accederse mediante un menú desplegable y usarse como anclas en la mayoría de los lectores.
# Los marcadores también pueden tener valores numéricos para los niveles de esquema,
# permitiendo que las entradas de esquema de nivel inferior oculten las entradas secundarias de nivel superior cuando se colapsan en el lector.
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
# Podemos eliminar dos elementos de modo que solo quede la designación del nivel de esquema para "Bookmark 1".
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# Hay nueve niveles de esquema. Su numeración se optimizará durante la operación de guardado.
# En este caso, los niveles "5" y "9" se convertirán en "2" y "3".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# Vaciar esta colección preservará los marcadores y los colocará todos en el mismo nivel de esquema.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

