---
title: MailMergeCleanupOptions enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies options that determine what items are removed during mail merge."
type: docs
weight: 90
url: /python-net/aspose.words.mailmerging/mailmergecleanupoptions/
---

## MailMergeCleanupOptions enumeration

Specifies options that determine what items are removed during mail merge.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies a default value. |
| REMOVE_EMPTY_PARAGRAPHS | Specifies whether paragraphs that contained mail merge fields with no data should be removed from the document. When this option is set, paragraphs which contain region start and end merge fields which are otherwise empty are also removed. |
| REMOVE_UNUSED_REGIONS | Specifies whether unused mail merge regions should be removed from the document. |
| REMOVE_UNUSED_FIELDS | Specifies whether unused merge fields should be removed from the document. |
| REMOVE_CONTAINING_FIELDS | Specifies whether fields that contain merge fields (for example, IFs) should be removed from the document if the nested merge fields are removed. |
| REMOVE_STATIC_FIELDS | Specifies whether static fields should be removed from the document. Static fields are fields, which results remain the same upon any document change. Fields, which do not store their results in a document and are calculated on the fly (like [FieldType.FIELD_LIST_NUM](../../aspose.words.fields/fieldtype/#FIELD_LIST_NUM), [FieldType.FIELD_SYMBOL](../../aspose.words.fields/fieldtype/#FIELD_SYMBOL), etc.) are not considered to be static. |
| REMOVE_EMPTY_TABLE_ROWS | Specifies whether empty rows that contain mail merge regions should be removed from the document. |

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

* module [aspose.words.mailmerging](../)

