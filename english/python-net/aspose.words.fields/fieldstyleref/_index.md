---
title: FieldStyleRef class
linktitle: FieldStyleRef class
articleTitle: FieldStyleRef class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldStyleRef class. Implements the STYLEREF field"
type: docs
weight: 980
url: /python-net/aspose.words.fields/fieldstyleref/
---

## FieldStyleRef class

Implements the STYLEREF field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




The STYLEREF is used to reference a fragment of text within the document that is formatted with
the specified style.


**Inheritance:** [FieldStyleRef](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldStyleRef()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_paragraph_number](./insert_paragraph_number/) | Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [insert_paragraph_number_in_full_context](./insert_paragraph_number_in_full_context/) | Gets or sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [insert_paragraph_number_in_relative_context](./insert_paragraph_number_in_relative_context/) | Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [insert_relative_position](./insert_relative_position/) | Gets or sets whether to insert the relative position of the referenced paragraph. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [search_from_bottom](./search_from_bottom/) | Gets or sets whether to search from the bottom of the current page, rather from the top. |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [style_name](./style_name/) | Gets or sets the name of the style by which the text to search for is formatted. |
| [suppress_non_delimiters](./suppress_non_delimiters/) | Gets or sets whether to suppress non-delimiter characters. |
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

Shows how to use STYLEREF fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a list based using a Microsoft Word list template.
list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)

# This generated list will display "1.a )".
# Space before the bracket is a non-delimiter character, which we can suppress.
list.list_levels[0].number_format = "\x0000."
list.list_levels[1].number_format = "\x0001 )"

# Add text and apply paragraph styles that STYLEREF fields will reference.
builder.list_format.list = list
builder.list_format.list_indent()
builder.paragraph_format.style = doc.styles.get_by_name("List Paragraph")
builder.writeln("Item 1")
builder.paragraph_format.style = doc.styles.get_by_name("Quote")
builder.writeln("Item 2")
builder.paragraph_format.style = doc.styles.get_by_name("List Paragraph")
builder.writeln("Item 3")
builder.list_format.remove_numbers()
builder.paragraph_format.style = doc.styles.get_by_name("Normal")

# Place a STYLEREF field in the header and display the first "List Paragraph"-styled text in the document.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(aw.fields.FieldType.FIELD_STYLE_REF, True).as_field_style_ref()
field.style_name = "List Paragraph"

# Place a STYLEREF field in the footer, and have it display the last text.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(aw.fields.FieldType.FIELD_STYLE_REF, True).as_field_style_ref()
field.style_name = "List Paragraph"
field.search_from_bottom = True

builder.move_to_document_end()

# We can also use STYLEREF fields to reference the list numbers of lists.
builder.write("\nParagraph number: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_STYLE_REF, True).as_field_style_ref()
field.style_name = "Quote"
field.insert_paragraph_number = True

builder.write("\nParagraph number, relative context: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_STYLE_REF, True).as_field_style_ref()
field.style_name = "Quote"
field.insert_paragraph_number_in_relative_context = True

builder.write("\nParagraph number, full context: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_STYLE_REF, True).as_field_style_ref()
field.style_name = "Quote"
field.insert_paragraph_number_in_full_context = True

builder.write("\nParagraph number, full context, non-delimiter chars suppressed: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_STYLE_REF, True).as_field_style_ref()
field.style_name = "Quote"
field.insert_paragraph_number_in_full_context = True
field.suppress_non_delimiters = True

doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_style_ref_paragraph_numbers.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

