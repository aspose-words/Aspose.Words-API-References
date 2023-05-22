---
title: MailMerge.merge_whole_document property
linktitle: merge_whole_document property
articleTitle: merge_whole_document property
second_title: Aspose.Words for Python
description: "MailMerge.merge_whole_document property. Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions."
type: docs
weight: 70
url: /python-net/aspose.words.mailmerging/mailmerge/merge_whole_document/
---

## MailMerge.merge_whole_document property

Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions.

The default value is ``False``.



### Examples

Shows the relationship between mail merges with regions, and field updating.

```python
def test_merge_whole_document(self):

    for merge_whole_document in (False, True):
        with self.subTest(merge_whole_document=merge_whole_document):
            doc = ExMailMerge.create_source_doc_merge_whole_document()
            data_table = ExMailMerge.create_source_table_merge_whole_document()

            # If we set the "merge_whole_document" flag to "True",
            # the mail merge with regions will update every field in the document.
            # If we set the "merge_whole_document" flag to "False", the mail merge will only update fields
            # within the mail merge region whose name matches the name of the data source table.
            doc.mail_merge.merge_whole_document = merge_whole_document
            doc.mail_merge.execute_with_regions(data_table)

            # The mail merge will only update the QUOTE field outside of the mail merge region
            # if we set the "merge_whole_document" flag to "True".
            doc.save(ARTIFACTS_DIR + "MailMerge.merge_whole_document.docx")

            self.assertTrue(doc.get_text().contains("This QUOTE field is inside the \"MyTable\" merge region."))
            self.assertEqual(merge_whole_document,
                doc.get_text().contains("This QUOTE field is outside of the \"MyTable\" merge region."))

@staticmethod
def create_source_doc_merge_whole_document() -> aw.Document:
    """Create a document with a mail merge region that belongs to a data source named "MyTable".
    Insert one QUOTE field inside this region, and one more outside it."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    field = builder.insert_field(aw.fields.field_type.FIELD_QUOTE, True).as_field_quote()
    field.text = "This QUOTE field is outside of the \"MyTable\" merge region."

    builder.insert_paragraph()
    builder.insert_field(" MERGEFIELD TableStart:MyTable")

    field = builder.insert_field(aw.fields.field_type.FIELD_QUOTE, True).as_field_quote()
    field.text = "This QUOTE field is inside the \"MyTable\" merge region."
    builder.insert_paragraph()

    builder.insert_field(" MERGEFIELD MyColumn")
    builder.insert_field(" MERGEFIELD TableEnd:MyTable")

    return doc

@staticmethod
def create_source_table_merge_whole_document() -> DataTable:
    """Create a data table that will be used in a mail merge."""

    data_table = DataTable("MyTable")
    data_table.columns.add("MyColumn")
    data_table.rows.add(["MyValue"])

    return data_table
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

