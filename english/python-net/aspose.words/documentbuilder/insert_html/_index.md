---
title: DocumentBuilder.insert_html method
linktitle: insert_html method
articleTitle: insert_html method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_html method"
type: docs
weight: 350
url: /python-net/aspose.words/documentbuilder/insert_html/
---

## insert_html(html) {#str}

Inserts an HTML string into the document.


```python
def insert_html(self, html: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | str |  |

You can use this method to insert an HTML fragment or whole HTML document.


## insert_html(html, use_builder_formatting) {#str_bool}

Inserts an HTML string into the document.


```python
def insert_html(self, html: str, use_builder_formatting: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | str |  |
| use_builder_formatting | bool |  |

You can use this method to insert an HTML fragment or whole HTML document.

When  is``False``,
[DocumentBuilder](../) formating is ignored and formatting of inserted text
is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.


When  is``True``,
formatting of inserted text is based on [DocumentBuilder](../) formatting,
and the text looks as if it were inserted with [DocumentBuilder.write()](../write/#str).





## insert_html(html, options) {#str_htmlinsertoptions}

Inserts an HTML string into the document. Allows to specify additional options.


```python
def insert_html(self, html: str, options: aspose.words.HtmlInsertOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| html | str |  |
| options | [HtmlInsertOptions](../../htmlinsertoptions/) |  |

You can use this method to insert an HTML fragment or whole HTML document.


## Examples

Shows how to use a document builder to insert html content into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

html = ("<p align='right'>Paragraph right</p>" +
        "<b>Implicit paragraph left</b>" +
        "<div align='center'>Div center</div>" +
        "<h1 align='left'>Heading 1 left.</h1>")

builder.insert_html(html)

# Inserting HTML code parses the formatting of each element into equivalent document text formatting.
paragraphs = doc.first_section.body.paragraphs

self.assertEqual("Paragraph right", paragraphs[0].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)

self.assertEqual("Implicit paragraph left", paragraphs[1].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertTrue(paragraphs[1].runs[0].font.bold)

self.assertEqual("Div center", paragraphs[2].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.CENTER, paragraphs[2].paragraph_format.alignment)

self.assertEqual("Heading 1 left.", paragraphs[3].get_text().strip())
self.assertEqual("Heading 1", paragraphs[3].paragraph_format.style.name)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_html.docx")
```

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

Shows how to apply a document builder's formatting while inserting HTML content.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
builder.paragraph_format.alignment = aw.ParagraphAlignment.DISTRIBUTED
builder.insert_html(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", use_builder_formatting)

paragraphs = doc.first_section.body.paragraphs

# The first paragraph has an alignment specified. When "insert_html" parses the HTML code,
# the paragraph alignment value found in the HTML code always supersedes the document builder's value.
self.assertEqual("Paragraph 1.", paragraphs[0].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)

# The second paragraph has no alignment specified. It can have its alignment value filled in
# by the builder's value depending on the flag we passed to the "insert_html" method.
self.assertEqual("Paragraph 2.", paragraphs[1].get_text().strip())
self.assertEqual(aw.ParagraphAlignment.DISTRIBUTED if use_builder_formatting else aw.ParagraphAlignment.LEFT,
    paragraphs[1].paragraph_format.alignment)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_html_with_formatting.docx")
```

Shows how to use options while inserting html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field(" MERGEFIELD Name ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD EMAIL ")
builder.insert_paragraph()

# By default "DocumentBuilder.insert_html" inserts a HTML fragment that ends with a block-level HTML element,
# it normally closes that block-level element and inserts a paragraph break.
# As a result, a new empty paragraph appears after inserted document.
# If we specify "HtmlInsertOptions.REMOVE_LAST_EMPTY_PARAGRAPH", those extra empty paragraphs will be removed.
builder.move_to_merge_field("NAME")
builder.insert_html("<p>John Smith</p>", aw.HtmlInsertOptions.USE_BUILDER_FORMATTING | aw.HtmlInsertOptions.REMOVE_LAST_EMPTY_PARAGRAPH)
builder.move_to_merge_field("EMAIL")
builder.insert_html("<p>jsmith@example.com</p>", aw.HtmlInsertOptions.USE_BUILDER_FORMATTING)

doc.save(ARTIFACTS_DIR + "MailMerge.remove_last_empty_paragraph.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

