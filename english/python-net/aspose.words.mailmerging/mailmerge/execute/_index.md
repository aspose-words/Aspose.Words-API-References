---
title: MailMerge.execute method
linktitle: execute method
articleTitle: execute method
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.MailMerge.execute method"
type: docs
weight: 180
url: /python-net/aspose.words.mailmerging/mailmerge/execute/
---

## execute(data_source) {#imailmergedatasource}

Performs a mail merge from a custom data source.


```python
def execute(self, data_source: aspose.words.mailmerging.IMailMergeDataSource):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_source | [IMailMergeDataSource](../../imailmergedatasource/) |  |

Use this method to fill mail merge fields in the document with values from
any data source such as a list or hashtable or objects. You need to write your
own class that implements the [IMailMergeDataSource](../../imailmergedatasource/) interface.

You can use this method only when [FieldOptions.is_bidi_text_supported_on_update](../../../aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/) is ``False``,
that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.

This method ignores the [MailMergeCleanupOptions.REMOVE_UNUSED_REGIONS](../../mailmergecleanupoptions/#REMOVE_UNUSED_REGIONS) option.




## execute(field_names, values) {#strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, field_names: List[str], values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_names | List[str] |  |
| values | List[object] |  |

Use this method to fill mail merge fields in the document with values from
an array of objects.

This method merges data for one record only. The array of field names
and the array of values represent the data of a single record.

This method does not use mail merge regions.

This method ignores the [MailMergeCleanupOptions.REMOVE_UNUSED_REGIONS](../../mailmergecleanupoptions/#REMOVE_UNUSED_REGIONS) option.




## Examples

Shows how to perform a mail merge, and then save the document to the client browser.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field(" MERGEFIELD FullName ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD Company ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD Address ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD City ")

doc.mail_merge.execute(["FullName", "Company", "Address", "City"],
    ["James Bond", "MI5 Headquarters", "Milbank", "London"])

# Send the document to the client browser.
with self.assertRaises(Exception):
    #Thrown because HttpResponse is null in the test.
    doc.save(response, "Artifacts/MailMerge.execute_array.docx", aw.ContentDisposition.INLINE, None)

# We will need to close this response manually to ensure that we do not add any superfluous content to the document after saving.
with self.assertRaises(Exception):
    response.end()
```

Shows how to merge an image from a URI as mail merge data into a MERGEFIELD.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# MERGEFIELDs with "Image:" tags will receive an image during a mail merge.
# The string after the colon in the "Image:" tag corresponds to a column name
# in the data source whose cells contain URIs of image files.
builder.insert_field("MERGEFIELD  Image:logo_FromWeb ")
builder.insert_field("MERGEFIELD  Image:logo_FromFileSystem ")

# Create a data source that contains URIs of images that we will merge.
# A URI can be a web URL that points to an image, or a local file system filename of an image file.
columns = ["logo_FromWeb", "logo_FromFileSystem"]
uris = [IMAGE_URL, IMAGE_DIR + "Logo.jpg"]

# Execute a mail merge on a data source with one row.
doc.mail_merge.execute(columns, uris)

doc.save(ARTIFACTS_DIR + "MailMergeEvent.image_from_url.docx")
```

## See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

