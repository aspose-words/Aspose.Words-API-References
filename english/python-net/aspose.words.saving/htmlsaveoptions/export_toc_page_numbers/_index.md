---
title: HtmlSaveOptions.export_toc_page_numbers property
linktitle: export_toc_page_numbers property
articleTitle: export_toc_page_numbers property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_toc_page_numbers property. Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB"
type: docs
weight: 280
url: /python-net/aspose.words.saving/htmlsaveoptions/export_toc_page_numbers/
---

## HtmlSaveOptions.export_toc_page_numbers property

Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB.
Default value is ``False``.



### Examples

Shows how to display page numbers when saving a document with a table of contents to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a table of contents, and then populate the document with paragraphs formatted using a "Heading"
# style that the table of contents will pick up as entries. Each entry will display the heading paragraph on the left,
# and the page number that contains the heading on the right.
field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()

builder.paragraph_format.style = builder.document.styles.get_by_name("Heading 1")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Entry 1")
builder.writeln("Entry 2")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Entry 3")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Entry 4")
field_toc.update_page_numbers()
doc.update_fields()

# HTML documents do not have pages. If we save this document to HTML,
# the page numbers that our TOC displays will have no meaning.
# When we save the document to HTML, we can pass a SaveOptions object to omit these page numbers from the TOC.
# If we set the "export_toc_page_numbers" flag to "True",
# each TOC entry will display the heading, separator, and page number, preserving its appearance in Microsoft Word.
# If we set the "export_toc_page_numbers" flag to "False",
# the save operation will omit both the separator and page number and leave the heading for each entry intact.
options = aw.saving.HtmlSaveOptions()
options.export_toc_page_numbers = export_toc_page_numbers

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.export_toc_page_numbers.html", options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.export_toc_page_numbers.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_toc_page_numbers:
    self.assertIn(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>", out_doc_contents)
else:
    self.assertIn(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

