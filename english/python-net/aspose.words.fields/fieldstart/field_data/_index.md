---
title: FieldStart.field_data property
linktitle: field_data property
articleTitle: field_data property
second_title: Aspose.Words for Python
description: "FieldStart.field_data property. Gets custom field data which is associated with the field."
type: docs
weight: 10
url: /python-net/aspose.words.fields/fieldstart/field_data/
---

## FieldStart.field_data property

Gets custom field data which is associated with the field.


```python
@property
def field_data(self) -> bytes:
    ...

```

### Examples

Shows how to get data associated with the field.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - Field with data.docx')
field = doc.range.fields[2]
print(system_helper.text.Encoding.get_string(field.start.field_data, system_helper.text.Encoding.utf_8()))
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldStart](../)

