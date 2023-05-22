---
title: FieldAddressBlock.get_field_names method
linktitle: get_field_names method
articleTitle: get_field_names method
second_title: Aspose.Words for Python
description: "FieldAddressBlock.get_field_names method. Returns a collection of mail merge field names used by the field."
type: docs
weight: 70
url: /python-net/aspose.words.fields/fieldaddressblock/get_field_names/
---

## get_field_names() {#default}

Returns a collection of mail merge field names used by the field.


```python
def get_field_names(self):
    ...
```

### Examples

Shows how to get mail merge field names used by a field.

```python
doc = aw.Document(MY_DIR + "Field sample - ADDRESSBLOCK.docx")

address_fields_expect = [
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
    ]

address_block_field = doc.range.fields[0].as_field_address_block()
address_block_field_names = address_block_field.get_field_names()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

