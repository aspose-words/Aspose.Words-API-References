---
title: Document.mail_merge property
linktitle: mail_merge property
articleTitle: mail_merge property
second_title: Aspose.Words for Python
description: "Document.mail_merge property. Returns a [MailMerge](../../../aspose.words.mailmerging/mailmerge/) object that represents the mail merge functionality for the document."
type: docs
weight: 270
url: /python-net/aspose.words/document/mail_merge/
---

## Document.mail_merge property

Returns a [MailMerge](../../../aspose.words.mailmerging/mailmerge/) object that represents the mail merge functionality for the document.



```python
@property
def mail_merge(self) -> aspose.words.mailmerging.MailMerge:
    ...

```

### Examples

Shows how to execute a mail merge with data from a DataTable.

```python
def test_execute_data_table(self):

    table = DataTable("Test")
    table.columns.add("CustomerName")
    table.columns.add("Address")
    table.rows.add(["Thomas Hardy", "120 Hanover Sq., London"])
    table.rows.add(["Paolo Accorti", "Via Monte Bianco 34, Torino"])

    # Below are two ways of using a DataTable as the data source for a mail merge.
    # 1 -  Use the entire table for the mail merge to create one output mail merge document for every row in the table:
    doc = ExMailMerge.create_source_doc_execute_data_table()

    doc.mail_merge.execute(table)

    doc.save(ARTIFACTS_DIR + "MailMerge.execute_data_table.whole_table.docx")

    # 2 -  Use one row of the table to create one output mail merge document:
    doc = ExMailMerge.create_source_doc_execute_data_table()

    doc.mail_merge.execute(table.rows[1])

    doc.save(ARTIFACTS_DIR + "MailMerge.execute_data_table.one_row.docx")

@staticmethod
def create_source_doc_execute_data_table() -> aw.Document:
    """Creates a mail merge source document."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.insert_field(" MERGEFIELD CustomerName ")
    builder.insert_paragraph()
    builder.insert_field(" MERGEFIELD Address ")

    return doc
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

