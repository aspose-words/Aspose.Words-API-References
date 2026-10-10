---
title: Bookmark.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Bookmark.name property. Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /ar/python-net/aspose.words/bookmark/name/
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
# الإشارة المرجعية الصالحة لها اسم وعقدة BookmarkStart وعقدة BookmarkEnd.
# أي مسافة بيضاء في أسماء الإشارات المرجعية سيتم تحويلها إلى شرطات سفلية إذا فتحنا المستند المحفوظ باستخدام Microsoft Word.
# إذا قمنا بتحديد اسم الإشارة المرجعية في Microsoft Word عبر إدراج -> روابط -> إشارة مرجعية، ثم ضغطنا على "انتقال إلى"،
# سوف يقفز المؤشر إلى النص المحاط بين عقدتي BookmarkStart وBookmarkEnd.
builder.start_bookmark('My Bookmark')
builder.write('Contents of MyBookmark.')
builder.end_bookmark('My Bookmark')
# الإشارات المرجعية مخزنة في هذه المجموعة.
self.assertEqual('My Bookmark', doc.range.bookmarks[0].name)
doc.save(file_name=ARTIFACTS_DIR + 'Bookmarks.Insert.docx')
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

