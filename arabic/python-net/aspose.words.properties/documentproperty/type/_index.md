---
title: DocumentProperty.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "DocumentProperty.type property. Gets the data type of the property."
type: docs
weight: 40
url: /ar/python-net/aspose.words.properties/documentproperty/type/
---

## DocumentProperty.type property

Gets the data type of the property.


```python
@property
def type(self) -> aspose.words.properties.PropertyType:
    ...

```

### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
# كائن "Document" يحتوي على بعض بياناته الوصفية في خصائصه.
print(f'Document filename:\n\t "{doc.original_file_name}"')
# المستند يخزن أيضًا البيانات الوصفية في خصائصه المدمجة.
# كل خاصية مدمجة هي عضو في كائن "BuiltInDocumentProperties" الخاص بالمستند.
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # بعض الخصائص قد تخزن قيمًا متعددة.
    if isinstance(doc_property.value, (list, tuple)):
        for value in doc_property.value:
            print(f'\tValue:\t"{value}"')
    else:
        print(f'\tValue:\t"{doc_property.value}"')
```

Shows how to work with a document's custom properties.

```python
import datetime
import aspose.words as aw
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# خصائص المستند المخصصة هي أزواج مفتاح-قيمة يمكننا إضافتها إلى المستند.
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=datetime.date.today())
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
# المجموعة ترتب الخصائص المخصصة بترتيب أبجدي.
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# اطبع كل خاصية مخصصة في المستند.
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# اعرض قيمة خاصية مخصصة باستخدام حقل DOCPROPERTY.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code=' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# يمكننا العثور على هذه الخصائص المخصصة في Microsoft Word عبر "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.DocumentPropertyCollection.docx')
# فيما يلي ثلاث طرق لإزالة الخصائص المخصصة من مستند.
# 1 -  إزالة حسب الفهرس:
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  إزالة حسب الاسم:
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  إفراغ المجموعة بالكامل مرة واحدة:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

