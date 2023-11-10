---
title: FieldToc class
linktitle: FieldToc class
articleTitle: FieldToc class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToc class. Implements the TOC field"
type: docs
weight: 1070
url: /python-net/aspose.words.fields/fieldtoc/
---

## FieldToc class

Implements the TOC field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds a table of contents (which can also be a table of figures) using the entries specified by TC fields,
their heading levels, and specified styles, and inserts that table at this place in the document.


**Inheritance:** [FieldToc](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToc()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [captionless_table_of_figures_label](./captionless_table_of_figures_label/) | Gets or sets the name of the sequence identifier used when building a table of figures that does not include caption's label and number. |
| [custom_styles](./custom_styles/) | Gets or sets a list of styles other than the built-in heading styles to include in the table of contents. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_identifier](./entry_identifier/) | Gets or sets a string that should match type identifiers of TC fields being included. |
| [entry_level_range](./entry_level_range/) | Gets or sets a range of levels of the table of contents entries to be included. |
| [entry_separator](./entry_separator/) | Gets or sets a sequence of characters that separate an entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [heading_level_range](./heading_level_range/) | Gets or sets a range of heading levels to include. |
| [hide_in_web_layout](./hide_in_web_layout/) | Gets or sets whether to hide tab leader and page numbers in Web layout view. |
| [insert_hyperlinks](./insert_hyperlinks/) | Gets or sets whether to make the table of contents entries hyperlinks. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_omitting_level_range](./page_number_omitting_level_range/) | Gets or sets a range of levels of the table of contents entries from which to omits page numbers. |
| [prefixed_sequence_identifier](./prefixed_sequence_identifier/) | Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number. |
| [preserve_line_breaks](./preserve_line_breaks/) | Gets or sets whether to preserve newline characters within table entries. |
| [preserve_tabs](./preserve_tabs/) | Gets or sets whether to preserve tab entries within table entries. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [table_of_figures_label](./table_of_figures_label/) | Gets or sets the name of the sequence identifier used when building a table of figures. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_paragraph_outline_level](./use_paragraph_outline_level/) | Gets or sets whether to use the applied paragraph outline level. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update_page_numbers()](./update_page_numbers/#default) | Updates the page numbers for items in this table of contents. |

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
def test_field_toc(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.start_bookmark("MyBookmark")

    # Insert a TOC field, which will compile all headings into a table of contents.
    # For each heading, this field will create a line with the text in that heading style to the left,
    # and the page the heading appears on to the right.
    field = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()

    # Use the "bookmark_name" property to only list headings
    # that appear within the bounds of a bookmark with the "MyBookmark" name.
    field.bookmark_name = "MyBookmark"

    # Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
    # We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
    field.custom_styles = "Quote; 6; Intense Quote; 7"

    # By default, Styles/TOC levels are separated in the "custom_styles" property by a comma,
    # but we can set a custom delimiter in this property.
    doc.field_options.custom_toc_style_separator = ";"

    # Configure the field to exclude any headings that have TOC levels outside of this range.
    field.heading_level_range = "1-3"

    # The TOC will not display the page numbers of headings whose TOC levels are within this range.
    field.page_number_omitting_level_range = "2-5"

    # Set a custom string that will separate every heading from its page number.
    field.entry_separator = "-"
    field.insert_hyperlinks = True
    field.hide_in_web_layout = False
    field.preserve_line_breaks = True
    field.preserve_tabs = True
    field.use_paragraph_outline_level = False

    ExField.insert_new_page_with_heading(builder, "First entry", "Heading 1")
    builder.writeln("Paragraph text.")
    ExField.insert_new_page_with_heading(builder, "Second entry", "Heading 1")
    ExField.insert_new_page_with_heading(builder, "Third entry", "Quote")
    ExField.insert_new_page_with_heading(builder, "Fourth entry", "Intense Quote")

    # These two headings will have the page numbers omitted because they are within the "2-5" range.
    ExField.insert_new_page_with_heading(builder, "Fifth entry", "Heading 2")
    ExField.insert_new_page_with_heading(builder, "Sixth entry", "Heading 3")

    # This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
    ExField.insert_new_page_with_heading(builder, "Seventh entry", "Heading 4")

    builder.end_bookmark("MyBookmark")
    builder.writeln("Paragraph text.")

    # This entry does not appear because it is outside the bookmark specified by the TOC.
    ExField.insert_new_page_with_heading(builder, "Eighth entry", "Heading 1")

    self.assertEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.get_field_code())

    field.update_page_numbers()
    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.field_toc.docx")

@staticmethod
def insert_new_page_with_heading(builder: aw.DocumentBuilder, caption_text: str, style_name: str):
    """Start a new page and insert a paragraph of a specified style."""

    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A TOC field can create an entry in its table of contents for each SEQ field found in the document.
# Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()

# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Use the "table_of_figures_label" property to name a main sequence for the TOC.
# Now, this TOC will only create entries out of SEQ fields with their "sequence_identifier" set to "MySequence".
field_toc.table_of_figures_label = "MySequence"

# We can name another SEQ field sequence in the "prefixed_sequence_identifier" property.
# SEQ fields from this prefix sequence will not create TOC entries.
# Every TOC entry created from a main sequence SEQ field will now also display the count that
# the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
field_toc.prefixed_sequence_identifier = "PrefixSequence"

# Each TOC entry will display the prefix sequence count immediately to the left
# of the page number that the main sequence SEQ field appears on.
# We can specify a custom separator that will appear between these two numbers.
field_toc.sequence_separator = ">"

self.assertEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", field_toc.get_field_code())

builder.insert_break(aw.BreakType.PAGE_BREAK)

# There are two ways of using SEQ fields to populate this TOC.
# 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
# This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
# Since this field does not belong to the main sequence identified
# by the "table_of_figures_label" property of the TOC, it will not appear as an entry.
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "PrefixSequence"
builder.insert_paragraph()

self.assertEqual(" SEQ  PrefixSequence", field_seq.get_field_code())

# 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
# This SEQ field will create an entry in the TOC.
# The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
# This entry will also display the count that the prefix sequence is currently at,
# separated from the page number by the value in the TOC's "seqence_separator" property.
# The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
# and the separator is ">", so entry will display "1>2".
builder.write("First TOC entry, MySequence #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"

self.assertEqual(" SEQ  MySequence", field_seq.get_field_code())

# Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
# The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
# so the TOC entry will display "2>3" at its page count.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "PrefixSequence"
builder.insert_paragraph()
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
builder.write("Second TOC entry, MySequence #")
field_seq.sequence_identifier = "MySequence"

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.toc_seq_prefix.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

