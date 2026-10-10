---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /es/python-net/aspose.words/bookmark/name/
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
# Un marcador válido tiene un nombre, un nodo BookmarkStart y un nodo BookmarkEnd.
# Cualquier espacio en blanco en los nombres de los marcadores se convertirá en guiones bajos si abrimos el documento guardado con Microsoft Word.
# Si resaltamos el nombre del marcador en Microsoft Word mediante Insertar -> Enlaces -> Marcador, y pulsamos "Go To",
# el cursor saltará al texto encerrado entre los nodos BookmarkStart y BookmarkEnd.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# Los marcadores se almacenan en esta colección.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

