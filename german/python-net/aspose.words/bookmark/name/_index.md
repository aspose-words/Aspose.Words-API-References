---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /de/python-net/aspose.words/bookmark/name/
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
# Ein gültiges Lesezeichen hat einen Namen, einen BookmarkStart- und einen BookmarkEnd-Knoten.
# Alle Leerzeichen in den Namen von Lesezeichen werden in Unterstriche umgewandelt, wenn wir das gespeicherte Dokument mit Microsoft Word öffnen.
# Wenn wir den Namen des Lesezeichens in Microsoft Word über Einfügen -> Links -> Lesezeichen markieren und "Gehe zu" drücken,
# springt der Cursor zum Text, der zwischen den BookmarkStart- und BookmarkEnd-Knoten eingeschlossen ist.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# Lesezeichen werden in dieser Sammlung gespeichert.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

