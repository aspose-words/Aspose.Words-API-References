---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /fr/python-net/aspose.words/bookmark/name/
---

## Bookmark.name property

Gets or sets the name of the bookmark.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Note that if you change the name of a bookmark to a name that already exists in the document,
no error will be given and only the first bookmark will be stored when you save the document.


### Examples

Shows how to insert a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Un signet valide possède un nom, un nœud BookmarkStart et un nœud BookmarkEnd.
# Tout espace dans les noms des signets sera converti en soulignés si nous ouvrons le document enregistré avec Microsoft Word.
# Si nous sélectionnons le nom du signet dans Microsoft Word via Insertion -> Liens -> Signet, et appuyons sur "Go To",
# le curseur sautera vers le texte encadré entre les nœuds BookmarkStart et BookmarkEnd.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# Les signets sont stockés dans cette collection.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

