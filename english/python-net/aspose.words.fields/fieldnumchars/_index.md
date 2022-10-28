---
title: FieldNumChars class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the NUMCHARS field"
type: docs
weight: 750
url: /python-net/aspose.words.fields/fieldnumchars/
---

## FieldNumChars class

Implements the NUMCHARS field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.




Retrieves the number of characters in the current document, as recorded in the **Characters** property of the
built-in document properties.



**Inheritance:** [FieldNumChars](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldNumChars()](./__init__/#default) | The default constructor. |

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

Shows how to use NUMCHARS, NUMWORDS, NUMPAGES and PAGE fields to track the size of our documents.

```python
doc = aw.Document(MY_DIR + "Paragraphs.docx")
builder = aw.DocumentBuilder(doc)

builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER

# Below are three types of fields that we can use to track the size of our documents.
# 1 -  Track the character count with a NUMCHARS field:
field_num_chars = builder.insert_field(aw.fields.FieldType.FIELD_NUM_CHARS, True).as_field_num_chars()
builder.writeln(" characters")

# 2 -  Track the word count with a NUMWORDS field:
field_num_words = builder.insert_field(aw.fields.FieldType.FIELD_NUM_WORDS, True).as_field_num_words()
builder.writeln(" words")

# 3 -  Use both PAGE and NUMPAGES fields to display what page the field is on,
# and the total number of pages in the document:
builder.paragraph_format.alignment = aw.ParagraphAlignment.RIGHT
builder.write("Page ")
field_page = builder.insert_field(aw.fields.FieldType.FIELD_PAGE, True).as_field_page()
builder.write(" of ")
field_num_pages = builder.insert_field(aw.fields.FieldType.FIELD_NUM_PAGES, True).as_field_num_pages()

self.assertEqual(" NUMCHARS ", field_num_chars.get_field_code())
self.assertEqual(" NUMWORDS ", field_num_words.get_field_code())
self.assertEqual(" NUMPAGES ", field_num_pages.get_field_code())
self.assertEqual(" PAGE ", field_page.get_field_code())

# These fields will not maintain accurate values in real time
# while we edit the document programmatically using Aspose.Words, or in Microsoft Word.
# We need to update them every we need to see an up-to-date value.
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_num.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

