---
title: image_field_merging method
second_title: Aspose.Words for Python via .NET API Reference
description: "Called when the Aspose.Words mail merge engine is about to insert an image into a merge field."
type: docs
weight: 20
url: /python-net/aspose.words.mailmerging/ifieldmergingcallback/image_field_merging/
---

## image_field_merging(args) {#imagefieldmergingargs}

Called when the Aspose.Words mail merge engine is about to insert an image into a merge field.


```python
def image_field_merging(self, args: aspose.words.mailmerging.ImageFieldMergingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [ImageFieldMergingArgs](../../imagefieldmergingargs/) |  |

### Examples

Shows how to insert images stored in a database BLOB field into a report.

```python
def test_image_from_blob(self):

    doc = aw.Document(MY_DIR + "Mail merge destination - Northwind employees.docx")

    doc.mail_merge.field_merging_callback = ExMailMergeEvent.HandleMergeImageFieldFromBlob()

    conn_string = f"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + 'Northwind.mdb'};"
    query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees"

    with OleDbConnection(conn_string) as conn:
        conn.open()

        # Open the data reader, which needs to be in a mode that reads all records at once.
        cmd = OleDbCommand(query, conn)
        data_reader = cmd.execute_reader()

        doc.mail_merge.execute_with_regions(data_reader, "Employees")

    doc.save(ARTIFACTS_DIR + "MailMergeEvent.image_from_blob.docx")

class HandleMergeImageFieldFromBlob(aw.mailmerging.IFieldMergingCallback):

    def field_merging(self, args: aw.mailmerging.FieldMergingArgs):

        # Do nothing.
        pass

    def image_field_merging(self, args: aw.mailmerging.ImageFieldMergingArgs):
        """This is called when a mail merge encounters a MERGEFIELD in the document with an "Image:" tag in its name."""

        args.image_stream = io.BytesIO(args.field_value)
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [IFieldMergingCallback](../)

