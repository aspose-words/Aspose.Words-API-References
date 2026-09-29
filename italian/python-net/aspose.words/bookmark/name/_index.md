---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /it/python-net/aspose.words/bookmark/name/
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
# Un segnalibro valido ha un nome, un nodo BookmarkStart e un nodo BookmarkEnd.
# Qualsiasi spazio nei nomi dei segnalibri verrà convertito in underscore se apriamo il documento salvato con Microsoft Word.
# Se evidenziamo il nome del segnalibro in Microsoft Word tramite Inserisci -> Collegamenti -> Segnalibro, e premiamo "Vai a",
# il cursore salterà al testo compreso tra i nodi BookmarkStart e BookmarkEnd.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# I segnalibri sono memorizzati in questa collezione.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

