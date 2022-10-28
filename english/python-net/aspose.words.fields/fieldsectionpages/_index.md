---
title: FieldSectionPages class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the SECTIONPAGES field"
type: docs
weight: 910
url: /python-net/aspose.words.fields/fieldsectionpages/
---

## FieldSectionPages class

Implements the SECTIONPAGES field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.




Retrieves the number of the current page within the current section.


**Inheritance:** [FieldSectionPages](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSectionPages()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
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

Shows how to use SECTION and SECTIONPAGES fields to number pages by sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.RIGHT

# A SECTION field displays the number of the section it is in.
builder.write("Section ")
field_section = builder.insert_field(aw.fields.FieldType.FIELD_SECTION, True).as_field_section()

self.assertEqual(" SECTION ", field_section.get_field_code())

# A PAGE field displays the number of the page it is in.
builder.write("\nPage ")
field_page = builder.insert_field(aw.fields.FieldType.FIELD_PAGE, True).as_field_page()

self.assertEqual(" PAGE ", field_page.get_field_code())

# A SECTIONPAGES field displays the number of pages that the section it is in spans across.
builder.write(" of ")
field_section_pages = builder.insert_field(aw.fields.FieldType.FIELD_SECTION_PAGES, True).as_field_section_pages()

self.assertEqual(" SECTIONPAGES ", field_section_pages.get_field_code())

# Move out of the header back into the main document and insert two pages.
# All these pages will be in the first section. Our fields, which appear once every header,
# will number the current/total pages of this section.
builder.move_to_document_end()
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)

# We can insert a new section with the document builder like this.
# This will affect the values displayed in the SECTION and SECTIONPAGES fields in all upcoming headers.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)

# The PAGE field will keep counting pages across the whole document.
# We can manually reset its count at each section to keep track of pages section-by-section.
builder.current_section.page_setup.restart_page_numbering = True
builder.insert_break(aw.BreakType.PAGE_BREAK)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_section.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

