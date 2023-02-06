---
title: FieldSeq class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the SEQ field"
type: docs
weight: 930
url: /python-net/aspose.words.fields/fieldseq/
---

## FieldSeq class

Implements the SEQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Sequentially numbers chapters, tables, figures, and other user-defined lists of items in a document.


**Inheritance:** [FieldSeq](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSeq()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_next_number](./insert_next_number/) | Gets or sets whether to insert the next sequence number for the specified item. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [reset_heading_level](./reset_heading_level/) | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [reset_number](./reset_number/) | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_identifier](./sequence_identifier/) | Gets or sets the name assigned to the series of items that are to be numbered. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

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

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Insert a SEQ field that will display the current count value of "MySequence",
# after using the "reset_number" property to set it to 100.
builder.write("#")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.reset_number = "100"
field_seq.update()

self.assertEqual(" SEQ  MySequence \\r 100", field_seq.get_field_code())
self.assertEqual("100", field_seq.result)

# Display the next number in this sequence with another SEQ field.
builder.write(", #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.update()

self.assertEqual("101", field_seq.result)

# Insert a level 1 heading.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name("Heading 1")
builder.writeln("This level 1 heading will reset MySequence to 1")
builder.paragraph_format.style = doc.styles.get_by_name("Normal")

# Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
builder.write("\n#")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.reset_heading_level = "1"
field_seq.update()

# The above heading is a level 1 heading, so the count for this sequence is reset to 1.
self.assertEqual(" SEQ  MySequence \\s 1", field_seq.get_field_code())
self.assertEqual("1", field_seq.result)

# Move to the next number of this sequence.
builder.write(", #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.insert_next_number = True
field_seq.update()

self.assertEqual(" SEQ  MySequence \\n", field_seq.get_field_code())
self.assertEqual("2", field_seq.result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.toc_seq_numbering.docx")
```

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A TOC field can create an entry in its table of contents for each SEQ field found in the document.
# Each entry contains the paragraph that contains the SEQ field,
# and the number of the page that the field appears on.
field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()

# Configure this TOC field to have a "sequence_identifier" property with a value of "MySequence".
field_toc.table_of_figures_label = "MySequence"

# Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
# named "TOCBookmark".
field_toc.bookmark_name = "TOCBookmark"
builder.insert_break(aw.BreakType.PAGE_BREAK)

self.assertEqual(" TOC  \\c MySequence \\b TOCBookmark", field_toc.get_field_code())

# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Insert a SEQ field that has a sequence identifier that matches the TOC's
# "table_of_figures_label" property. This field will not create an entry in the TOC since it is outside
# the bookmark's bounds designated by "BookmarkName".
builder.write("MySequence #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
builder.writeln(", will not show up in the TOC because it is outside of the bookmark.")

builder.start_bookmark("TOCBookmark")

# This SEQ field's sequence matches the TOC's "table_of_figures_label" property and is within the bookmark's bounds.
# The paragraph that contains this field will show up in the TOC as an entry.
builder.write("MySequence #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
builder.writeln(", will show up in the TOC next to the entry for the above caption.")

# This SEQ field's sequence does not match the TOC's "table_of_figures_label" property,
# and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
builder.write("MySequence #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "OtherSequence"
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")

# This SEQ field's sequence matches the TOC's "table_of_figures_label" property and is within the bounds of the bookmark.
# This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
# The SEQ field itself will not display the contents of that bookmark.
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.bookmark_name = "SEQBookmark"
self.assertEqual(" SEQ  MySequence SEQBookmark", field_seq.get_field_code())

# Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark("SEQBookmark")
builder.write("MySequence #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
builder.writeln(", text from inside SEQBookmark.")
builder.end_bookmark("SEQBookmark")

builder.end_bookmark("TOCBookmark")

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.toc_seq_bookmark.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

