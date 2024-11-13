---
title: CustomDocumentProperties.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.properties.CustomDocumentProperties.add method"
type: docs
weight: 20
url: /python-net/aspose.words.properties/customdocumentproperties/add/
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
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# Custom document properties are key-value pairs that we can add to the document.
properties.add('Authorized', True)
properties.add('Authorized By', 'John Doe')
properties.add('Authorized Date', datetime.datetime.now())
properties.add('Authorized Revision', doc.built_in_document_properties.revision_number)
properties.add('Authorized Amount', 123.45)
# The collection sorts the custom properties in alphabetic order.
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# Print every custom property in the document.
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# Display the value of a custom property using a DOCPROPERTY field.
builder = aw.DocumentBuilder(doc)
field = builder.insert_field(' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(ARTIFACTS_DIR + 'DocumentProperties.document_property_collection.docx')
# Below are three ways or removing custom properties from a document.
# 1 -  Remove by index:
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  Remove by name:
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  Empty the entire collection at once:
properties.clear()
self.assertEqual(0, properties.count)
```

Shows how to create a custom document property which contains a date and time.

```python
doc = aw.Document()
doc.custom_document_properties.add(name='AuthorizationDate', value=datetime.datetime.now())
authorization_date = doc.custom_document_properties.get_by_name('AuthorizationDate').to_date_time()
print(f'Document authorized on {authorization_date}')
```

## See Also

* module [aspose.words.properties](../../)
* class [CustomDocumentProperties](../)

