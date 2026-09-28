---
title: FieldComments.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldComments.text property. Gets or sets the text of the comments."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldcomments/text/
---

## FieldComments.text property

Gets or sets the text of the comments.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the COMMENTS field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# حدد قيمة لخاصية \"Comments\" المدمجة في المستند.
doc.built_in_document_properties.comments = 'My comment.'
# أنشئ حقل COMMENTS لعرض قيمة تلك الخاصية المدمجة.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True).as_field_comments()
field.update()
self.assertEqual(' COMMENTS ', field.get_field_code())
self.assertEqual('My comment.', field.result)
# إذا أعطينا خاصية Text لحقل COMMENTS قيمة وقمنا بتحديثه، سيقوم الحقل بـ
# استبدال القيمة الحالية لخاصية \"Comments\" المدمجة بقيمة خاصية Text الخاصة به،
# ثم عرض القيمة الجديدة.
field.text = 'My overriding comment.'
field.update()
self.assertEqual(' COMMENTS  "My overriding comment."', field.get_field_code())
self.assertEqual('My overriding comment.', field.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMMENTS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldComments](../)

