---
title: to_double method
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns the property value as double."
type: docs
weight: 90
url: /python-net/aspose.words.properties/documentproperty/to_double/
---

## to_double() {#default}

Returns the property value as double.


```python
def to_double(self):
    ...
```

Throws an exception if the property type is not [PropertyType.NUMBER](../../propertytype/#NUMBER).



### Examples

Shows various type conversion methods of custom document properties.

```python
doc = aw.Document()
properties = doc.custom_document_properties

auth_date = datetime.now()
properties.add("Authorized", True)
properties.add("Authorized By", "John Doe")
properties.add("Authorized Date", auth_date)
properties.add("Authorized Revision", doc.built_in_document_properties.revision_number)
properties.add("Authorized Amount", 123.45)

self.assertEqual(True, properties.get_by_name("Authorized").to_bool())
self.assertEqual("John Doe", str(properties.get_by_name("Authorized By")))
self.assertEqual(auth_date, properties.get_by_name("Authorized Date").to_date_time())
self.assertEqual(1, properties.get_by_name("Authorized Revision").to_int())
self.assertEqual(123.45, properties.get_by_name("Authorized Amount").to_double())
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

