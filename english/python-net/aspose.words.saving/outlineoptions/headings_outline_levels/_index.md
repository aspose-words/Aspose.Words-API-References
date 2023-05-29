---
title: OutlineOptions.headings_outline_levels property
linktitle: headings_outline_levels property
articleTitle: headings_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.headings_outline_levels property. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline."
type: docs
weight: 70
url: /python-net/aspose.words.saving/outlineoptions/headings_outline_levels/
---

## OutlineOptions.headings_outline_levels property

Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the 
document outline.

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert headings of levels 1 to 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1

self.assertTrue(builder.paragraph_format.is_heading)

builder.writeln("Heading 1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2

builder.writeln("Heading 1.1")
builder.writeln("Heading 1.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3

builder.writeln("Heading 1.2.1")
builder.writeln("Heading 1.2.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4

builder.writeln("Heading 1.2.2.1")
builder.writeln("Heading 1.2.2.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5

builder.writeln("Heading 1.2.2.2.1")
builder.writeln("Heading 1.2.2.2.2")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "headings_outline_levels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.outline_options.headings_outline_levels = 4

# If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
# an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
# In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
# the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
# In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
# Set the "expanded_outline_levels" property to "2" to automatically expand all heading level 2 and lower outline entries
# and collapse all level and 3 and higher entries when we open the document.
options.outline_options.expanded_outline_levels = 2

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.expanded_outline_levels.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

