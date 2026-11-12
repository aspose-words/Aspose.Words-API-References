---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /tr/python-net/aspose.words/bookmark/name/
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
# Geçerli bir yer imi bir ada, bir BookmarkStart ve bir BookmarkEnd düğümüne sahiptir.
# Yer imlerinin adlarındaki boşluklar, kaydedilen belgeyi Microsoft Word ile açarsak alt çizgilere dönüştürülecektir.
# Microsoft Word'de Insert -> Links -> Bookmark yoluyla yer imi adını vurgular ve \"Go To\" tuşuna basarsak,
# imleç, BookmarkStart ve BookmarkEnd düğümleri arasında bulunan metne atlayacaktır.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# Yer imleri bu koleksiyonda depolanır.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

