---
title: DocumentProperty.to_date_time method
linktitle: to_date_time method
articleTitle: to_date_time method
second_title: Aspose.Words for Python
description: "DocumentProperty.to_date_time method. Returns the property value as DateTime in UTC."
type: docs
weight: 80
url: /python-net/aspose.words.properties/documentproperty/to_date_time/
---

## to_date_time() {#default}

Returns the property value as **DateTime** in UTC.



```python
def to_date_time(self):
    ...
```

### Remarks

Throws an exception if the property type is not [PropertyType.DATE_TIME](../../propertytype/#DATE_TIME).

Microsoft Word stores only the date part (no time) for custom date properties.




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

Shows how to create a custom document property which contains a date and time.

```python
doc = aw.Document()
doc.custom_document_properties.add('AuthorizationDate', datetime.datetime.utcnow())
print('Document authorized on', doc.custom_document_properties.get_by_name('AuthorizationDate').to_date_time())
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

