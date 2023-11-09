---
title: MailMergeSettings.header_source property
linktitle: header_source property
articleTitle: header_source property
second_title: Aspose.Words for Python
description: "MailMergeSettings.header_source property. Specifies the path to the mail-merge header source"
type: docs
weight: 100
url: /python-net/aspose.words.settings/mailmergesettings/header_source/
---

## MailMergeSettings.header_source property

Specifies the path to the mail-merge header source.
The default value is an empty string.


```python
@property
def header_source(self) -> str:
    ...

@header_source.setter
def header_source(self, value: str):
    ...

```

### Examples

Shows how to construct a data source for a mail merge from a header source and a data source.

```python
# Create a mailing label merge header file, which will consist of a table with one row.
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.start_table()
builder.insert_cell()
builder.write("FirstName")
builder.insert_cell()
builder.write("LastName")
builder.end_table()

doc.save(ARTIFACTS_DIR + "MailMerge.mailing_label_merge.header.docx")

# Create a mailing label merge data file consisting of a table with one row
# and the same number of columns as the header document's table.
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.start_table()
builder.insert_cell()
builder.write("John")
builder.insert_cell()
builder.write("Doe")
builder.end_table()

doc.save(ARTIFACTS_DIR + "MailMerge.mailing_label_merge.data.docx")

# Create a merge destination document with MERGEFIELDS with names that
# match the column names in the merge header file table.
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Dear ")
builder.insert_field("MERGEFIELD FirstName", "<FirstName>")
builder.write(" ")
builder.insert_field("MERGEFIELD LastName", "<LastName>")

settings = doc.mail_merge_settings

# Construct a data source for our mail merge by specifying two document filenames.
# The header source will name the columns of the data source table.
settings.header_source = ARTIFACTS_DIR + "MailMerge.mailing_label_merge.header.docx"

# The data source will provide rows of data for all the columns in the header document table.
settings.data_source = ARTIFACTS_DIR + "MailMerge.mailing_label_merge.data.docx"

# Configure a mailing label type mail merge, which Microsoft Word will execute
# as soon as we use it to load the output document.
settings.query = "SELECT * FROM " + settings.data_source
settings.main_document_type = aw.settings.MailMergeMainDocumentType.MAILING_LABELS
settings.data_type = aw.settings.MailMergeDataType.TEXT_FILE
settings.link_to_query = True
settings.view_merged_data = True

doc.save(ARTIFACTS_DIR + "MailMerge.mailing_label_merge.docx")
```

### See Also

* module [aspose.words.settings](../../)
* class [MailMergeSettings](../)

