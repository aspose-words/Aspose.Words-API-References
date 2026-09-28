---
title: FieldSet.bookmark_text property
linktitle: bookmark_text property
articleTitle: bookmark_text property
second_title: Aspose.Words for Python
description: "FieldSet.bookmark_text property. Gets or sets the new text of the bookmark."
type: docs
weight: 30
url: /ar/python-net/aspose.words.fields/fieldset/bookmark_text/
---

## FieldSet.bookmark_text property

Gets or sets the new text of the bookmark.


```python
@property
def bookmark_text(self) -> str:
    ...

@bookmark_text.setter
def bookmark_text(self, value: str):
    ...

```

### Examples

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# تسمية النص المؤشر عليه بعلامة مرجعية باستخدام حقل SET.
# يشير هذا الحقل إلى "bookmark" وليس إلى بنية علامة مرجعية تظهر داخل النص، بل إلى متغيّر مسمى.
field_set = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SET, update_field=False).as_field_set()
field_set.bookmark_name = 'MyBookmark'
field_set.bookmark_text = 'Hello world!'
field_set.update()
self.assertEqual(' SET  MyBookmark "Hello world!"', field_set.get_field_code())
# أشر إلى العلامة المرجعية بالاسم في حقل REF وعرض محتوياتها.
field_ref = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
field_ref.bookmark_name = 'MyBookmark'
field_ref.update()
self.assertEqual(' REF  MyBookmark', field_ref.get_field_code())
self.assertEqual('Hello world!', field_ref.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.SET.REF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSet](../)

