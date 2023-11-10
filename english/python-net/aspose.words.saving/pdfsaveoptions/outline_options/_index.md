---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 240
url: /python-net/aspose.words.saving/pdfsaveoptions/outline_options/
---

## PdfSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outline_options](./) class.




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

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert headings that can serve as TOC entries of levels 1 and 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1

self.assertTrue(builder.paragraph_format.is_heading)

builder.writeln("Heading 1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5

builder.writeln("Heading 1.1.1.1.1")
builder.writeln("Heading 1.1.1.1.2")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()

# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "headings_outline_levels" property to "5" to include all headings of levels 5 and below in the outline.
save_options.outline_options.headings_outline_levels = 5

# This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
# The output PDF document will treat outline levels 2, 3, and 4 as "missing".
# Set the "create_missing_outline_levels" property to "True" to include all missing levels in the outline,
# leaving blank outline entries since there are no usable headings.
# Set the "create_missing_outline_levels" property to "False" to ignore missing outline levels,
# and treat the outline level 5 headings as level 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.create_missing_outline_levels.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

