---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /sv/python-net/aspose.words/bookmark/name/
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
# Ett giltigt bokmärke har ett namn, en BookmarkStart och en BookmarkEnd-nod.
# Alla blanksteg i bokmärkens namn kommer att konverteras till understreck om vi öppnar det sparade dokumentet med Microsoft Word.
# Om vi markerar bokmärkets namn i Microsoft Word via Infoga -> Länkar -> Bokmärke och trycker på \"Go To\",
# kommer markören att hoppa till texten som är innesluten mellan BookmarkStart- och BookmarkEnd-noderna.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# Bokmärken lagras i denna samling.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

