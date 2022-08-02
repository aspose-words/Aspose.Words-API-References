---
title: page_number_style property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the page number format."
type: docs
weight: 310
url: /python-net/aspose.words/pagesetup/page_number_style/
---

## PageSetup.page_number_style property

Gets or sets the page number format.


### Examples

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Section 1, page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Section 1, page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Section 1, page 3.")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln("Section 2, page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Section 2, page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Section 2, page 3.")

# Move the document builder to the first section's primary header,
# which every page in that section will display.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)

# Insert a PAGE field, which will display the number of the current page.
builder.write("Page ")
builder.insert_field("PAGE", "")

# Configure the section to have the page count that PAGE fields display start from 5.
# Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN

# Create another primary header for the second section, with another PAGE field.
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(" - ")
builder.insert_field("PAGE", "")
builder.write(" - ")

# Configure the section to have the page count that PAGE fields display start from 10.
# Also, configure all PAGE fields to display their page numbers using Arabic numbers.
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC

doc.save(ARTIFACTS_DIR + "PageSetup.page_numbering.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

