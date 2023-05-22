---
title: FieldMergingArgs.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldMergingArgs.text property. Gets or sets the text that will be inserted into the document for the current merge field."
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/fieldmergingargs/text/
---

## FieldMergingArgs.text property

Gets or sets the text that will be inserted into the document for the current merge field.

When your event handler is called, this property is set to ``None``.

If you leave Text as ``None``, the mail merge engine will insert [FieldMergingArgsBase.field_value](../../fieldmergingargsbase/field_value/) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.




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

* module [aspose.words.mailmerging](../../)
* class [FieldMergingArgs](../)

