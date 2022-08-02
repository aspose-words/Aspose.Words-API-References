---
title: use_whole_paragraph_as_region property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value indicating whether whole paragraph with TableStart or TableEnd field or particular range between TableStart and TableEnd fields should be included into mail merge region."
type: docs
weight: 160
url: /python-net/aspose.words.mailmerging/mailmerge/use_whole_paragraph_as_region/
---

## MailMerge.use_whole_paragraph_as_region property

Gets or sets a value indicating whether whole paragraph with TableStart or TableEnd field
or particular range between TableStart and TableEnd fields should be included into mail merge region.

The default value is **true**.



### Examples

Shows the relationship between mail merge regions and paragraphs.

```python
def test_use_whole_paragraph_as_region(self):

    for use_whole_paragraph_as_region in (False, True):
        with self.subTest(use_whole_paragraph_as_region=use_whole_paragraph_as_region):
            doc = ExMailMerge.create_source_doc_with_nested_merge_regions()
            data_table = ExMailMerge.create_source_table_data_table_for_one_region()

            # By default, a paragraph can belong to no more than one mail merge region.
            # The contents of our document do not meet these criteria.
            # If we set the "use_whole_paragraph_as_region" flag to "True",
            # running a mail merge on this document will throw an exception.
            # If we set the "use_whole_paragraph_as_region" flag to "False",
            # we will be able to execute a mail merge on this document.
            doc.mail_merge.use_whole_paragraph_as_region = use_whole_paragraph_as_region

            if use_whole_paragraph_as_region:
                with self.assertRaises(Exception):
                    doc.mail_merge.execute_with_regions(data_table)
            else:
                doc.mail_merge.execute_with_regions(data_table)

            # The mail merge populates our first region while leaving the second region unused
            # since it is the region that breaks the rule.
            doc.save(ARTIFACTS_DIR + "MailMerge.use_whole_paragraph_as_region.docx")

@staticmethod
def create_source_doc_with_nested_merge_regions() -> aw.Document:
    """Create a document with two mail merge regions sharing one paragraph."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.write("Region 1: ")
    builder.insert_field(" MERGEFIELD TableStart:MyTable")
    builder.insert_field(" MERGEFIELD Column1")
    builder.write(", ")
    builder.insert_field(" MERGEFIELD Column2")
    builder.insert_field(" MERGEFIELD TableEnd:MyTable")

    builder.write(", Region 2: ")
    builder.insert_field(" MERGEFIELD TableStart:MyOtherTable")
    builder.insert_field(" MERGEFIELD TableEnd:MyOtherTable")

    return doc

@staticmethod
def create_source_table_data_table_for_one_region() -> DataTable:
    """Create a data table that can populate one region during a mail merge."""

    data_table = DataTable("MyTable")
    data_table.columns.add("Column1")
    data_table.columns.add("Column2")
    data_table.rows.add(["Value 1", "Value 2"])

    return data_table
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

