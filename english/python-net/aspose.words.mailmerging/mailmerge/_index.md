﻿---
title: MailMerge class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents the mail merge functionality"
type: docs
weight: 80
url: /python-net/aspose.words.mailmerging/mailmerge/
---

## MailMerge class

Represents the mail merge functionality.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




For mail merge operation to work, the document should contain Word MERGEFIELD and
optionally NEXT fields. During mail merge operation, merge fields in the document are
replaced with values from your data source.

There are two distinct ways to use mail merge: with mail merge regions and without.

The simplest mail merge is without regions and it is very similar to how mail merge
works in Word. Use ``Execute`` methods to merge information from some
data source such as **DataTable**, **DataSet**, **DataView**, **IDataReader**
or an array of objects into your document. The
[MailMerge](./) object processes all records of the data source and copies and appends
content of the whole document for each record.

Note that when [MailMerge](./) object encounters a NEXT field, it selects next record
in the data source and continues merging without copying any content.

Use [MailMerge.execute_with_regions()](./execute_with_regions/#imailmergedatasource) and other overloads to merge information into a
document with mail merge regions defined. You can use
**DataSet**, **DataTable**, **DataView** or **IDataReader**
as data sources for this operation.

You need to use mail merge regions if you want to dynamically grow portions inside the
document. Without mail merge regions whole document will be repeated for every record of
the data source.




### Properties

| Name | Description |
| --- | --- |
| [cleanup_options](./cleanup_options/) | Gets or sets a set of flags that specify what items should be removed during mail merge. |
| [cleanup_paragraphs_with_punctuation_marks](./cleanup_paragraphs_with_punctuation_marks/) | Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS](../mailmergecleanupoptions/#REMOVE_EMPTY_PARAGRAPHS) option is specified. |
| [field_merging_callback](./field_merging_callback/) | Occurs during mail merge when a mail merge field is encountered in the document. |
| [mail_merge_callback](./mail_merge_callback/) | Allows to handle particular events during mail merge. |
| [mapped_data_fields](./mapped_data_fields/) | Returns a collection that represents mapped data fields for the mail merge operation. |
| [merge_duplicate_regions](./merge_duplicate_regions/) | Gets or sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [merge_whole_document](./merge_whole_document/) | Gets or sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [preserve_unused_tags](./preserve_unused_tags/) | Gets or sets a value indicating whether the unused "mustache" tags should be preserved. |
| [region_end_tag](./region_end_tag/) | Gets or sets a mail merge region end tag. |
| [region_start_tag](./region_start_tag/) | Gets or sets a mail merge region start tag. |
| [restart_lists_at_each_section](./restart_lists_at_each_section/) | Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [retain_first_section_start](./retain_first_section_start/) | Gets or sets a value indicating whether the [PageSetup.section_start](../../aspose.words/pagesetup/section_start/) of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [trim_whitespaces](./trim_whitespaces/) | Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [unconditional_merge_fields_and_regions](./unconditional_merge_fields_and_regions/) | Gets or sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [use_non_merge_fields](./use_non_merge_fields/) | When ``True``, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags. |
| [use_whole_paragraph_as_region](./use_whole_paragraph_as_region/) | Gets or sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |

### Methods

| Name | Description |
| --- | --- |
|[ delete_fields()](./delete_fields/#default) | Removes mail merge related fields from the document. |
|[ execute(data_source)](./execute/#imailmergedatasource) | Performs a mail merge from a custom data source. |
|[ execute(field_names, values)](./execute/#strlist_objectlist) | Performs a mail merge operation for a single record. |
|[ execute_with_regions(data_source)](./execute_with_regions/#imailmergedatasource) | Performs a mail merge from a custom data source with mail merge regions. |
|[ execute_with_regions(data_source_root)](./execute_with_regions/#imailmergedatasourceroot) | Performs a mail merge from a custom data source with mail merge regions. |
|[ get_field_names()](./get_field_names/#default) | Returns a collection of mail merge field names available in the document. |
|[ get_field_names_for_region(region_name)](./get_field_names_for_region/#str) | Returns a collection of mail merge field names available in the region. |
|[ get_field_names_for_region(region_name, region_index)](./get_field_names_for_region/#str_int) | Returns a collection of mail merge field names available in the region. |
|[ get_regions_by_name(region_name)](./get_regions_by_name/#str) | Returns a collection of mail merge regions with the specified name. |
|[ get_regions_hierarchy()](./get_regions_hierarchy/#default) | Returns a full hierarchy of regions (with fields) available in the document. |

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

* module [aspose.words.mailmerging](../)
* class [Document](../../aspose.words/document/)
* property [Document.mail_merge](../../aspose.words/document/mail_merge/)

