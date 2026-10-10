---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/field/is_dirty/
---

## Field.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.


```python
@property
def is_dirty(self) -> bool:
    ...

@is_dirty.setter
def is_dirty(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أعط قيمة الخاصية المدمجة "Author" في المستند، ثم اعرضها باستخدام حقل.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# قم بتحديث الخاصية. لا يزال الحقل يعرض القيمة القديمة.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# نظرًا لأن قيمة الحقل قديمة، يمكننا وضع علامة "dirty" عليها.
# ستظل هذه القيمة غير محدثة حتى نقوم بتحديث الحقل يدويًا باستخدام طريقة Field.Update().
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # إذا حفظنا دون استدعاء طريقة تحديث،
    # سيستمر الحقل في عرض القيمة غير المحدثة في المستند الناتج.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # كائن LoadOptions يحتوي على خيار لتحديث جميع الحقول
    # يتم وضع علامة "dirty" عليها عند تحميل المستند.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # تحديث الحقول المتسخة بهذه الطريقة يضبط تلقائيًا علم "IsDirty" الخاص بها إلى false.
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

