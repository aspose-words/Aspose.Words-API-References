---
title: CustomDocumentProperties.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.properties.CustomDocumentProperties.add method"
type: docs
weight: 20
url: /zh/python-net/aspose.words.properties/customdocumentproperties/add/
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
# 自定义文档属性是我们可以添加到文档的键值对。
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=datetime.date.today())
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
# 该集合按字母顺序对自定义属性进行排序。
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# 打印文档中的每个自定义属性。
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# 使用 DOCPROPERTY 字段显示自定义属性的值。
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code=' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# 我们可以在 Microsoft Word 中通过 “File” -> “Properties” > “Advanced Properties” > “Custom” 找到这些自定义属性。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.DocumentPropertyCollection.docx')
# 下面是从文档中删除自定义属性的三种方法。
# 1 -  按索引删除：
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  按名称删除：
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  一次性清空整个集合：
properties.clear()
self.assertEqual(0, properties.count)
```

## See Also

* module [aspose.words.properties](../../)
* class [CustomDocumentProperties](../)

