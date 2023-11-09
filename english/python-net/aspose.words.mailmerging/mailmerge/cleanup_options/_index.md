---
title: MailMerge.cleanup_options property
linktitle: cleanup_options property
articleTitle: cleanup_options property
second_title: Aspose.Words for Python
description: "MailMerge.cleanup_options property. Gets or sets a set of flags that specify what items should be removed during mail merge."
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/mailmerge/cleanup_options/
---

## MailMerge.cleanup_options property

Gets or sets a set of flags that specify what items should be removed during mail merge.


```python
@property
def cleanup_options(self) -> aspose.words.mailmerging.MailMergeCleanupOptions:
    ...

@cleanup_options.setter
def cleanup_options(self, value: aspose.words.mailmerging.MailMergeCleanupOptions):
    ...

```

### Examples

Shows how to automatically remove MERGEFIELDs that go unused during mail merge.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a document with MERGEFIELDs for three columns of a mail merge data source table,
# and then create a table with only two columns whose names match our MERGEFIELDs.
builder.insert_field(" MERGEFIELD FirstName ")
builder.write(" ")
builder.insert_field(" MERGEFIELD LastName ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD City ")

data_table = DataTable("MyTable")
data_table.columns.add("FirstName")
data_table.columns.add("LastName")
data_table.rows.add(["John", "Doe"])
data_table.rows.add(["Joe", "Bloggs"])

# Our third MERGEFIELD references a "City" column, which does not exist in our data source.
# The mail merge will leave fields such as this intact in their pre-merge state.
# Setting the "cleanup_options" property to "REMOVE_UNUSED_FIELDS" will remove any MERGEFIELDs
# that go unused during a mail merge to clean up the merge documents.
doc.mail_merge.cleanup_options = mail_merge_cleanup_options
doc.mail_merge.execute(data_table)

if mail_merge_cleanup_options in (aw.mailmerging.MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS, aw.mailmerging.MailMergeCleanupOptions.REMOVE_STATIC_FIELDS):
    self.assertEqual(0, doc.range.fields.count)
else:
    self.assertEqual(2, doc.range.fields.count)
```

Shows how to remove empty paragraphs that a mail merge may create from the merge output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field(" MERGEFIELD TableStart:MyTable")
builder.insert_field(" MERGEFIELD FirstName ")
builder.write(" ")
builder.insert_field(" MERGEFIELD LastName ")
builder.insert_field(" MERGEFIELD TableEnd:MyTable")

data_table = DataTable("MyTable")
data_table.columns.add("FirstName")
data_table.columns.add("LastName")
data_table.rows.add(["John", "Doe"])
data_table.rows.add(["", ""])
data_table.rows.add(["Jane", "Doe"])

doc.mail_merge.cleanup_options = mail_merge_cleanup_options
doc.mail_merge.execute_with_regions(data_table)

if doc.mail_merge.cleanup_options == aw.mailmerging.MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS:
    self.assertEqual(
        "John Doe\r" +
        "Jane Doe", doc.get_text().strip())
else:
    self.assertEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.get_text().strip())
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

