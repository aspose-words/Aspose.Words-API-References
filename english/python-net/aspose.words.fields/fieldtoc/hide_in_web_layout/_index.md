---
title: FieldToc.hide_in_web_layout property
linktitle: hide_in_web_layout property
articleTitle: hide_in_web_layout property
second_title: Aspose.Words for Python
description: "FieldToc.hide_in_web_layout property. Gets or sets whether to hide tab leader and page numbers in Web layout view."
type: docs
weight: 90
url: /python-net/aspose.words.fields/fieldtoc/hide_in_web_layout/
---

## FieldToc.hide_in_web_layout property

Gets or sets whether to hide tab leader and page numbers in Web layout view.


```python
@property
def hide_in_web_layout(self) -> bool:
    ...

@hide_in_web_layout.setter
def hide_in_web_layout(self, value: bool):
    ...

```

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
def field_toc():
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    builder.start_bookmark('MyBookmark')
    # Insert a TOC field, which will compile all headings into a table of contents.
    # For each heading, this field will create a line with the text in that heading style to the left,
    # and the page the heading appears on to the right.
    field = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()
    # Use the "bookmark_name" property to only list headings
    # that appear within the bounds of a bookmark with the "MyBookmark" name.
    field.bookmark_name = 'MyBookmark'
    # Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
    # We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
    field.custom_styles = 'Quote; 6; Intense Quote; 7'
    # By default, Styles/TOC levels are separated in the "custom_styles" property by a comma,
    # but we can set a custom delimiter in this property.
    doc.field_options.custom_toc_style_separator = ';'
    # Configure the field to exclude any headings that have TOC levels outside of this range.
    field.heading_level_range = '1-3'
    # The TOC will not display the page numbers of headings whose TOC levels are within this range.
    field.page_number_omitting_level_range = '2-5'
    # Set a custom string that will separate every heading from its page number.
    field.entry_separator = '-'
    field.insert_hyperlinks = True
    field.hide_in_web_layout = False
    field.preserve_line_breaks = True
    field.preserve_tabs = True
    field.use_paragraph_outline_level = False
    insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
    builder.writeln('Paragraph text.')
    insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
    insert_new_page_with_heading(builder, 'Third entry', 'Quote')
    insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
    # These two headings will have the page numbers omitted because they are within the "2-5" range.
    insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
    insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
    # This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
    insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
    builder.end_bookmark('MyBookmark')
    builder.writeln('Paragraph text.')
    # This entry does not appear because it is outside the bookmark specified by the TOC.
    insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
    self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w', field.get_field_code())
    field.update_page_numbers()
    doc.update_fields()
    doc.save(ARTIFACTS_DIR + 'Field.field_toc.docx')

def insert_new_page_with_heading(builder: aw.DocumentBuilder, caption_text: str, style_name: str):
    """Start a new page and insert a paragraph of a specified style."""
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

