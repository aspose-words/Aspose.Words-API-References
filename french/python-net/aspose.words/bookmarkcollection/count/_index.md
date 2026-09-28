---
title: BookmarkCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "BookmarkCollection.count property. Returns the number of bookmarks in the collection."
type: docs
weight: 20
url: /fr/python-net/aspose.words/bookmarkcollection/count/
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
# Insérez cinq signets avec du texte à l'intérieur de leurs limites.
i = 1
while i <= 5:
    bookmark_name = 'MyBookmark_' + str(i)
    builder.start_bookmark(bookmark_name)
    builder.write(f'Text inside {bookmark_name}.')
    builder.end_bookmark(bookmark_name)
    builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
    i += 1
# Cette collection stocke les signets.
bookmarks = doc.range.bookmarks
self.assertEqual(5, bookmarks.count)
# Il existe plusieurs façons de supprimer des signets.
# 1 -  Appel de la méthode Remove du signet :
bookmarks.get_by_name('MyBookmark_1').remove()
self.assertFalse(any([b.name == 'MyBookmark_1' for b in bookmarks]))
# 2 -  Passage du signet à la méthode Remove de la collection :
bookmark = doc.range.bookmarks[0]
doc.range.bookmarks.remove(bookmark=bookmark)
self.assertFalse(any([b.name == 'MyBookmark_2' for b in bookmarks]))
# 3 -  Suppression d'un signet de la collection par son nom :
doc.range.bookmarks.remove(bookmark_name='MyBookmark_3')
self.assertFalse(any([b.name == 'MyBookmark_3' for b in bookmarks]))
# 4 -  Suppression d'un signet à un indice dans la collection de signets :
doc.range.bookmarks.remove_at(0)
self.assertFalse(any([b.name == 'MyBookmark_4' for b in bookmarks]))
# Nous pouvons vider toute la collection de signets.
bookmarks.clear()
# Le texte qui était à l'intérieur des signets est toujours présent dans le document.
self.assertEqual(0, bookmarks.count)
self.assertEqual('Text inside MyBookmark_1.\r' + 'Text inside MyBookmark_2.\r' + 'Text inside MyBookmark_3.\r' + 'Text inside MyBookmark_4.\r' + 'Text inside MyBookmark_5.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [BookmarkCollection](../)

