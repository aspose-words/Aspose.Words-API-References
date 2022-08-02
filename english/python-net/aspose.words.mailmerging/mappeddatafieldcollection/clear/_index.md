---
title: clear method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes all elements from the collection."
type: docs
weight: 30
url: /python-net/aspose.words.mailmerging/mappeddatafieldcollection/clear/
---

## clear() {#default}

Removes all elements from the collection.


```python
def clear(self):
    ...
```

### Examples

Shows how to map data columns and MERGEFIELDs with different names so the data is transferred between them during a mail merge.

```python
def test_mapped_data_field_collection(self):

    doc = ExMailMerge.create_source_doc_mapped_data_fields()
    data_table = ExMailMerge.create_source_table_mapped_fata_fields()

    # The table has a column named "Column2", but there are no MERGEFIELDs with that name.
    # Also, we have a MERGEFIELD named "Column3", but the data source does not have a column with that name.
    # If data from "Column2" is suitable for the "Column3" MERGEFIELD,
    # we can map that column name to the MERGEFIELD in the "MappedDataFields" key/value pair.
    mapped_data_fields = doc.mail_merge.mapped_data_fields

    # We can link a data source column name to a MERGEFIELD name like this.
    mapped_data_fields.add("MergeFieldName", "DataSourceColumnName")

    # Link the data source column named "Column2" to MERGEFIELDs named "Column3".
    mapped_data_fields.add("Column3", "Column2")

    # The MERGEFIELD name is the "key" to the respective data source column name "value".
    self.assertEqual("DataSourceColumnName", mapped_data_fields["MergeFieldName"])
    self.assertTrue(mapped_data_fields.contains_key("MergeFieldName"))
    self.assertTrue(mapped_data_fields.contains_value("DataSourceColumnName"))

    # Now if we run this mail merge, the "Column3" MERGEFIELDs will take data from "Column2" of the table.
    doc.mail_merge.execute(data_table)

    doc.save(ARTIFACTS_DIR + "MailMerge.mapped_data_field_collection.docx")

    # We can iterate over the elements in this collection.
    self.assertEqual(2, mapped_data_fields.count)

    for field in mapped_data_fields:
        print(f"Column named {field.value} is mapped to MERGEFIELDs named {field.key}")

    # We can also remove elements from the collection.
    mapped_data_fields.remove("MergeFieldName")

    self.assertFalse(mapped_data_fields.contains_key("MergeFieldName"))
    self.assertFalse(mapped_data_fields.contains_value("DataSourceColumnName"))

    mapped_data_fields.clear()

    self.assertEqual(0, mapped_data_fields.count)

@staticmethod
def create_source_doc_mapped_data_fields() -> aw.Document:
    """Create a document with 2 MERGEFIELDs, one of which does not have a
    corresponding column in the data table from the method below."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.insert_field(" MERGEFIELD Column1")
    builder.write(", ")
    builder.insert_field(" MERGEFIELD Column3")

    return doc

@staticmethod
def create_source_table_mapped_fata_fields() -> DataTable:
    """Create a data table with 2 columns, one of which does not have a
    corresponding MERGEFIELD in the source document from the method above."""

    data_table = DataTable("MyTable")
    data_table.columns.add("Column1")
    data_table.columns.add("Column2")
    data_table.rows.add(["Value1", "Value2"])

    return data_table
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MappedDataFieldCollection](../)

