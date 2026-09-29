---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /ru/python-net/aspose.words/bookmark/name/
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
# Действительная закладка имеет имя, узел BookmarkStart и узел BookmarkEnd.
# Любые пробелы в названиях закладок будут преобразованы в подчёркивания, если мы откроем сохранённый документ в Microsoft Word.
# Если мы выделим имя закладки в Microsoft Word через Insert -> Links -> Bookmark и нажмём "Go To",
# курсор перейдёт к тексту, заключённому между узлами BookmarkStart и BookmarkEnd.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# Закладки хранятся в этой коллекции.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

