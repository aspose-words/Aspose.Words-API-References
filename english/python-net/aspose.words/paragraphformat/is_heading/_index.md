---
title: ParagraphFormat.is_heading property
linktitle: is_heading property
articleTitle: is_heading property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_heading property. True when the paragraph style is one of the built-in Heading styles."
type: docs
weight: 130
url: /python-net/aspose.words/paragraphformat/is_heading/
---

## ParagraphFormat.is_heading property

True when the paragraph style is one of the built-in Heading styles.


### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1

self.assertTrue(builder.paragraph_format.is_heading)

builder.writeln("Heading 1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2

builder.writeln("Heading 1.1")
builder.writeln("Heading 1.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3

builder.writeln("Heading 1.2.1")
builder.writeln("Heading 1.2.2")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF

# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "headings_outline_levels" property to "2" to exclude all headings whose levels are above 2 from the outline.
# The last two headings we have inserted above will not appear.
save_options.outline_options.headings_outline_levels = 2

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.headings_outline_levels.pdf", save_options)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

