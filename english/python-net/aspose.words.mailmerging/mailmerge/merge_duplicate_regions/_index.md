---
title: MailMerge.merge_duplicate_regions property
linktitle: merge_duplicate_regions property
articleTitle: merge_duplicate_regions property
second_title: Aspose.Words for Python
description: "MailMerge.merge_duplicate_regions property. Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one."
type: docs
weight: 60
url: /python-net/aspose.words.mailmerging/mailmerge/merge_duplicate_regions/
---

## MailMerge.merge_duplicate_regions property

Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source
should be merged while executing of a mail merge with regions against the data source or just the first one.

The default value is ``False``.



### Examples

Shows how to work with duplicate mail merge regions.

```python
def test_merge_duplicate_regions(self):

    for merge_duplicate_regions in (True, False):
        with self.subTest(merge_duplicate_regions=merge_duplicate_regions):
            doc = ExMailMerge.create_source_doc_merge_duplicate_regions()
            data_table = ExMailMerge.create_source_table_merge_duplicate_regions()

            # If we set the "merge_duplicate_regions" property to "False", the mail merge will affect the first region,
            # while the MERGEFIELDs of the second one will be left in the pre-merge state.
            # To get both regions merged like that,
            # we would have to execute the mail merge twice on a table of the same name.
            # If we set the "merge_duplicate_regions" property to "True", the mail merge will affect both regions.
            doc.mail_merge.merge_duplicate_regions = merge_duplicate_regions

            doc.mail_merge.execute_with_regions(data_table)
            doc.save(ARTIFACTS_DIR + "MailMerge.merge_duplicate_regions.docx")

@staticmethod
def create_source_doc_merge_duplicate_regions() -> aw.Document:
    """Returns a document that contains two duplicate mail merge regions (sharing the same name in the "TableStart/End" tags)."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.insert_field(" MERGEFIELD TableStart:MergeRegion")
    builder.insert_field(" MERGEFIELD Column1")
    builder.insert_field(" MERGEFIELD TableEnd:MergeRegion")
    builder.insert_paragraph()

    builder.insert_field(" MERGEFIELD TableStart:MergeRegion")
    builder.insert_field(" MERGEFIELD Column2")
    builder.insert_field(" MERGEFIELD TableEnd:MergeRegion")

    return doc

@staticmethod
def create_source_table_merge_duplicate_regions() -> DataTable:
    """Creates a data table with one row and two columns."""

    data_table = DataTable("MergeRegion")
    data_table.columns.add("Column1")
    data_table.columns.add("Column2")
    data_table.rows.add(["Value 1", "Value 2"])

    return data_table
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

