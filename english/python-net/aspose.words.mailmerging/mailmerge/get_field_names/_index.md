---
title: MailMerge.get_field_names method
linktitle: get_field_names method
articleTitle: get_field_names method
second_title: Aspose.Words for Python
description: "MailMerge.get_field_names method. Returns a collection of mail merge field names available in the document."
type: docs
weight: 200
url: /python-net/aspose.words.mailmerging/mailmerge/get_field_names/
---

## get_field_names() {#default}

Returns a collection of mail merge field names available in the document.


```python
def get_field_names(self):
    ...
```

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

A new string array is created on every call.

Includes "mustache" field names if [MailMerge.use_non_merge_fields](../use_non_merge_fields/) is ``True``.




### Examples

Shows how to get names of all merge fields in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field(" MERGEFIELD FirstName ")
builder.write(" ")
builder.insert_field(" MERGEFIELD LastName ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD City ")

data_table = DataTable("MyTable")
data_table.columns.add("FirstName")
data_table.columns.add("LastName")
data_table.columns.add("City")
data_table.rows.add(["John", "Doe", "New York"])
data_table.rows.add(["Joe", "Bloggs", "Washington"])

# For every MERGEFIELD name in the document, ensure that the data table contains a column
# with the same name, and then execute the mail merge.
field_names = doc.mail_merge.get_field_names()

self.assertEqual(3, len(field_names))

for field_name in field_names:
    self.assertTrue(data_table.columns.contains(field_name))

doc.mail_merge.execute(data_table)
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

