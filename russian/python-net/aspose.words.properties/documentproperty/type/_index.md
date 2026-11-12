---
title: DocumentProperty.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "DocumentProperty.type property. Gets the data type of the property."
type: docs
weight: 40
url: /ru/python-net/aspose.words.properties/documentproperty/type/
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
# Объект "Document" содержит часть своей метаданных в своих членах.
print(f'Document filename:\n\t "{doc.original_file_name}"')
# Документ также сохраняет метаданные во встроенных свойствах.
# Каждое встроенное свойство является членом объекта "BuiltInDocumentProperties" документа.
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # Некоторые свойства могут хранить несколько значений.
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
# Пользовательские свойства документа — это пары «ключ‑значение», которые мы можем добавить в документ.
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=datetime.date.today())
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
# Коллекция сортирует пользовательские свойства в алфавитном порядке.
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# Выведите каждое пользовательское свойство в документе.
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# Отобразите значение пользовательского свойства с помощью поля DOCPROPERTY.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code=' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# Мы можем найти эти пользовательские свойства в Microsoft Word через "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.DocumentPropertyCollection.docx')
# Ниже представлены три способа удаления пользовательских свойств из документа.
# 1 -  Удалить по индексу:
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  Удалить по имени:
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  Очистить всю коллекцию сразу:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

