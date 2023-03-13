﻿---
title: FieldMergingArgs class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides data for the MergeField event"
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/fieldmergingargs/
---

## FieldMergingArgs class

Provides data for the **MergeField** event.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




The **MergeField** event occurs during mail merge when a simple mail merge
field is encountered in the document. You can respond to this event to return
text for the mail merge engine to insert into the document.




**Inheritance:** [FieldMergingArgs](./) → [FieldMergingArgsBase](../fieldmergingargsbase/)

### Properties

| Name | Description |
| --- | --- |
| [document](../fieldmergingargsbase/document/) | Returns the [FieldMergingArgsBase.document](../fieldmergingargsbase/document/) object for which the mail merge is performed.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [document_field_name](../fieldmergingargsbase/document_field_name/) | Gets the name of the merge field as specified in the document.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field](../fieldmergingargsbase/field/) | Gets the object that represents the current merge field.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field_name](../fieldmergingargsbase/field_name/) | Gets the name of the merge field in the data source.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [field_value](../fieldmergingargsbase/field_value/) | Gets or sets the value of the field from the data source.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [record_index](../fieldmergingargsbase/record_index/) | Gets the zero based index of the record that is being merged.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [table_name](../fieldmergingargsbase/table_name/) | Gets the name of the data table for the current merge operation or empty string if the name is not available.<br>(Inherited from [FieldMergingArgsBase](../fieldmergingargsbase/)) |
| [text](./text/) | Gets or sets the text that will be inserted into the document for the current merge field. |

### Examples

Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents.

```python
def test_merge_html(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.insert_field(r"MERGEFIELD  html_Title  \b Content")
    builder.insert_field(r"MERGEFIELD  html_Body  \b Content")

    merge_data = [
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>",

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    ]

    doc.mail_merge.field_merging_callback = ExMailMergeEvent.HandleMergeFieldInsertHtml()
    doc.mail_merge.execute(["html_Title", "html_Body"], merge_data)

    doc.save(ARTIFACTS_DIR + "MailMergeEvent.merge_html.docx")

class HandleMergeFieldInsertHtml(aw.mailmerging.IFieldMergingCallback):
    """If the mail merge encounters a MERGEFIELD whose name starts with the "html_" prefix,
    this callback parses its merge data as HTML content and adds the result to the document location of the MERGEFIELD."""

    def field_merging(self, args: aw.mailmerging.FieldMergingArgs):
        """Called when a mail merge merges data into a MERGEFIELD."""

        if args.document_field_name.startswith("html_") and "\\b" in args.field.get_field_code():

            # Add parsed HTML data to the document's body.
            builder = aw.DocumentBuilder(args.document)
            builder.move_to_merge_field(args.document_field_name)
            builder.insert_html(str(args.field_value))

            # Since we have already inserted the merged content manually,
            # we will not need to respond to this event by returning content via the "text" property.
            args.text = ""

    def image_field_merging(self, args: aw.mailmerging.ImageFieldMergingArgs):

        # Do nothing.
        pass
```

### See Also

* module [aspose.words.mailmerging](../)
* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* class [IFieldMergingCallback](../ifieldmergingcallback/)

