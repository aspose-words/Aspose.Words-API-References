---
title: ImageFieldMergingArgs class
linktitle: ImageFieldMergingArgs class
articleTitle: ImageFieldMergingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.ImageFieldMergingArgs class. Provides data for the [IFieldMergingCallback.image_field_merging()](../ifieldmergingcallback/image_field_merging/#imagefieldmergingargs) event"
type: docs
weight: 70
url: /python-net/aspose.words.mailmerging/imagefieldmergingargs/
---

## ImageFieldMergingArgs class

Provides data for the [IFieldMergingCallback.image_field_merging()](../ifieldmergingcallback/image_field_merging/#imagefieldmergingargs) event.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




This event occurs during mail merge when an image mail merge
field is encountered in the document. You can respond to this event to return a
file name, stream, or an SkiaSharp.SKBitmap object to the mail merge
engine so it is inserted into the document.

There are three properties available [ImageFieldMergingArgs.image_file_name](./image_file_name/),
[ImageFieldMergingArgs.image_stream](./image_stream/) and Aspose.Words.MailMerging.ImageFieldMergingArgs.Image to specify where the image must be taken from.
Set only one of these properties.

To insert an image mail merge field into a document in Word, select Insert/Field command,
then select MergeField and type Image:MyFieldName.




**Inheritance:** [ImageFieldMergingArgs](./) → [FieldMergingArgsBase](../fieldmergingargsbase/)

### Properties

| Name | Description |
| --- | --- |
| [document](../fieldmergingargsbase/document/) | Returns the [FieldMergingArgsBase.document](../fieldmergingargsbase/document/) object for which the mail merge is performed.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [document_field_name](../fieldmergingargsbase/document_field_name/) | Gets the name of the merge field as specified in the document.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field](../fieldmergingargsbase/field/) | Gets the object that represents the current merge field.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field_name](../fieldmergingargsbase/field_name/) | Gets the name of the merge field in the data source.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field_value](../fieldmergingargsbase/field_value/) | Gets or sets the value of the field from the data source.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [image_file_name](./image_file_name/) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [image_height](./image_height/) | Specifies the image height for the image to insert into the document. |
| [image_stream](./image_stream/) | Specifies the stream for the mail merge engine to read an image from. |
| [image_width](./image_width/) | Specifies the image width for the image to insert into the document. |
| [record_index](../fieldmergingargsbase/record_index/) | Gets the zero based index of the record that is being merged.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [shape](./shape/) | Specifies the shape that the mail merge engine must insert into the document. |
| [table_name](../fieldmergingargsbase/table_name/) | Gets the name of the data table for the current merge operation or empty string if the name is not available.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |

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

* module [aspose.words.mailmerging](../)
* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* class [IFieldMergingCallback](../ifieldmergingcallback/)

