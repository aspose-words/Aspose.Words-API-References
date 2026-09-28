---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /ar/python-net/aspose.words.fields/fieldoptions/default_document_author/
---

## FieldOptions.default_document_author property

Gets or sets default document author's name. If author's name is already specified in built-in document properties,
this option is not considered.


```python
@property
def default_document_author(self) -> str:
    ...

@default_document_author.setter
def default_document_author(self, value: str):
    ...

```

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# تحصل حقول AUTHOR على نتائجها من خاصية المستند المدمجة المسماة "Author".
# إذا أنشأنا وحفظنا مستندًا في Microsoft Word،
# سيحتوي على اسم المستخدم الخاص بنا في تلك الخاصية.
# ومع ذلك، إذا أنشأنا مستندًا برمجيًا باستخدام Aspose.Words،
# ستكون خاصية "Author"، بشكل افتراضي، سلسلة فارغة.
self.assertEqual('', doc.built_in_document_properties.author)
# حدد اسم مؤلف احتياطي لاستخدامه في حقول AUTHOR
# إذا كانت خاصية "Author" تحتوي على سلسلة فارغة.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# تحديث حقل AUTHOR الذي يحتوي على قيمة
# سيطبق تلك القيمة على الخاصية المدمجة "Author".
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# تغيير هذه الخاصية، ثم تحديث حقل AUTHOR سيطبق هذه القيمة على الحقل.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# إذا قمنا بتحديث حقل AUTHOR بعد تغيير خاصية "Name" الخاصة به،
# سوف يعرض الحقل الاسم الجديد ويطبق الاسم الجديد على الخاصية المدمجة.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# حقول AUTHOR لا تؤثر على خاصية DefaultDocumentAuthor.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

