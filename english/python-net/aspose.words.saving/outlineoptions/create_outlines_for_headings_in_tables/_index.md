---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
---

## OutlineOptions.create_outlines_for_headings_in_tables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```python
@property
def create_outlines_for_headings_in_tables(self) -> bool:
    ...

@create_outlines_for_headings_in_tables.setter
def create_outlines_for_headings_in_tables(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Create a table with three rows. The first row,
# whose text we will format in a heading-type style, will serve as the column header.
builder.start_table()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('Customers')
builder.end_row()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.write('John Doe')
builder.end_row()
builder.insert_cell()
builder.write('Jane Doe')
builder.end_table()
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "headings_outline_levels" property to "1" to get the outline
# to only register headings with heading levels that are no larger than 1.
pdf_save_options.outline_options.headings_outline_levels = 1
# Set the "create_outlines_for_headings_in_tables" property to "False" to exclude all headings within tables,
# such as the one we have created above from the outline.
# Set the "create_outlines_for_headings_in_tables" property to "True" to include all headings within tables
# in the outline, provided that they have a heading level that is no larger than the value of the "headings_outline_levels" property.
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.table_heading_outlines.pdf', pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

