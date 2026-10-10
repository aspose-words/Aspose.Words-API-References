---
title: BookmarksOutlineLevelCollection indexer
linktitle: BookmarksOutlineLevelCollection indexer
articleTitle: BookmarksOutlineLevelCollection indexer
second_title: Aspose.Words for Python
description: "BookmarksOutlineLevelCollection indexer. Gets or sets a bookmark outline level at the specified index."
type: docs
weight: 20
url: /fr/python-net/aspose.words.saving/bookmarksoutlinelevelcollection/__getitem__/
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
# Insérez un signet avec un autre signet imbriqué à l'intérieur.
builder.start_bookmark('Bookmark 1')
builder.writeln('Text inside Bookmark 1.')
builder.start_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1 and 2.')
builder.end_bookmark('Bookmark 2')
builder.writeln('Text inside Bookmark 1.')
builder.end_bookmark('Bookmark 1')
# Insérez un autre signet.
builder.start_bookmark('Bookmark 3')
builder.writeln('Text inside Bookmark 3.')
builder.end_bookmark('Bookmark 3')
# Lors de l'enregistrement au format .pdf, les signets peuvent être accessibles via un menu déroulant et utilisés comme ancres par la plupart des lecteurs.
# Les signets peuvent également avoir des valeurs numériques pour les niveaux de plan,
# permettant aux entrées de plan de niveau inférieur de masquer les entrées enfants de niveau supérieur lorsqu'elles sont réduites dans le lecteur.
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
# Nous pouvons supprimer deux éléments afin qu'il ne reste que la désignation du niveau de plan pour "Bookmark 1".
outline_levels.remove_at(2)
outline_levels.remove('Bookmark 2')
# Il existe neuf niveaux de plan. Leur numérotation sera optimisée pendant l'opération d'enregistrement.
# Dans ce cas, les niveaux "5" et "9" deviendront "2" et "3".
outline_levels.add('Bookmark 2', 5)
outline_levels.add('Bookmark 3', 9)
doc.save(file_name=ARTIFACTS_DIR + 'BookmarksOutlineLevelCollection.BookmarkLevels.pdf', save_options=pdf_save_options)
# Vider cette collection préservera les signets et les placera tous au même niveau de plan.
outline_levels.clear()
```

### See Also

* module [aspose.words.saving](../../)
* class [BookmarksOutlineLevelCollection](../)

