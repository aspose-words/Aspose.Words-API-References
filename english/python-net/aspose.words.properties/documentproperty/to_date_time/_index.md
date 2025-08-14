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

Shows how to create a custom document property which contains a date and time.

```python
doc = aw.Document()
doc.custom_document_properties.add(name='AuthorizationDate', value=datetime.datetime.now())
authorization_date = doc.custom_document_properties.get_by_name('AuthorizationDate').to_date_time()
print(f'Document authorized on {authorization_date}')
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

