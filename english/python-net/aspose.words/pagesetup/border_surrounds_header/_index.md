---
title: border_surrounds_header property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the page border includes or excludes the header."
type: docs
weight: 60
url: /python-net/aspose.words/pagesetup/border_surrounds_header/
---

## PageSetup.border_surrounds_header property

Specifies whether the page border includes or excludes the header.

Note, changing this property affects all sections in the document.


### Examples

Shows how to apply a border to the page and header/footer.

```python
doc = aw.Document()

builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world! This is the main body text.")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write("This is the header.")
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write("This is the footer.")
builder.move_to_document_end()

# Insert a blue double-line border.
page_setup = doc.sections[0].page_setup
page_setup.borders.line_style = aw.LineStyle.DOUBLE
page_setup.borders.color = drawing.Color.blue

# A section's PageSetup object has "border_surrounds_header" and "border_surrounds_footer" flags that determine
# whether a page border surrounds the main body text, also includes the header or footer, respectively.
# Set the "border_surrounds_header" flag to "True" to surround the header with our border,
# and then set the "border_surrounds_footer" flag to leave the footer outside of the border.
page_setup.border_surrounds_header = True
page_setup.border_surrounds_footer = False

doc.save(ARTIFACTS_DIR + "PageSetup.page_border.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

