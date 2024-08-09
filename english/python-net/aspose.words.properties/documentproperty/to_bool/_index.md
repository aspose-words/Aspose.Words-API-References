---
title: DocumentProperty.to_bool method
linktitle: to_bool method
articleTitle: to_bool method
second_title: Aspose.Words for Python
description: "DocumentProperty.to_bool method. Returns the property value as bool."
type: docs
weight: 60
url: /python-net/aspose.words.properties/documentproperty/to_bool/
---

## to_bool() {#default}

Returns the property value as bool.


```python
def to_bool(self):
    ...
```

### Remarks

Throws an exception if the property type is not [PropertyType.BOOLEAN](../../propertytype/#BOOLEAN).




### Examples

Shows various type conversion methods of custom document properties.

```python
doc = aw.Document()
properties = doc.custom_document_properties
auth_date = datetime.date.today()
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=auth_date)
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
self.assertEqual(True, properties.get_by_name('Authorized').to_bool())
self.assertEqual('John Doe', properties.get_by_name('Authorized By').to_string())
self.assertEqual(auth_date, properties.get_by_name('Authorized Date').to_date_time())
self.assertEqual(1, properties.get_by_name('Authorized Revision').to_int())
self.assertEqual(123.45, properties.get_by_name('Authorized Amount').to_double())
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

