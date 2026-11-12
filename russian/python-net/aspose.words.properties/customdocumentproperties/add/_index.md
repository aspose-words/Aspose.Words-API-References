---
title: CustomDocumentProperties.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.properties.CustomDocumentProperties.add method"
type: docs
weight: 20
url: /ru/python-net/aspose.words.properties/customdocumentproperties/add/
---

## add(name, value) {#str_str}

Creates a new custom document property of the [PropertyType.STRING](../../propertytype/#STRING) data type.



```python
def add(self, name: str, value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the property. |
| value | str | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#str_int}

Creates a new custom document property of the [PropertyType.NUMBER](../../propertytype/#NUMBER) data type.



```python
def add(self, name: str, value: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the property. |
| value | int | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#str_datetime}

Creates a new custom document property of the [PropertyType.DATE_TIME](../../propertytype/#DATE_TIME) data type.



```python
def add(self, name: str, value: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the property. |
| value | datetime.datetime | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#str_bool}

Creates a new custom document property of the [PropertyType.BOOLEAN](../../propertytype/#BOOLEAN) data type.



```python
def add(self, name: str, value: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the property. |
| value | bool | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#str_float}

Creates a new custom document property of the [PropertyType.DOUBLE](../../propertytype/#DOUBLE) data type.



```python
def add(self, name: str, value: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the property. |
| value | float | The value of the property. |

### Returns

The newly created property object.


## Examples

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

## See Also

* module [aspose.words.properties](../../)
* class [CustomDocumentProperties](../)

