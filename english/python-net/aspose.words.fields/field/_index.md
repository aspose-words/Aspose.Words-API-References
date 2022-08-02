---
title: Field class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a Microsoft Word document field."
type: docs
weight: 50
url: /python-net/aspose.words.fields/field/
---

## Field class

Represents a Microsoft Word document field.


A field in a Word document is a complex structure consisting of multiple nodes that include field start,
field code, field separator, field result and field end. Fields can be nested, contain rich content and span
multiple paragraphs or sections in a document. The [Field](./) class is a "facade" object that provides
properties and methods that allow to work with a field as a single object. 

The [Field.start](./start/), [Field.separator](./separator/) and [Field.end](./end/) properties point to the
field start, separator and end nodes of the field respectively.

The content between the field start and separator is the field code. The content between the
field separator and field end is the field result. The field code typically consists of one or more
[Run](../../aspose.words/run/) objects that specify instructions. The processing application is expected to execute
the field code to calculate the field result.

The process of calculating field results is called the field update. Aspose.Words can update field
results of most of the field types in exactly the same way as Microsoft Word does it. Most notably,
Aspose.Words can calculate results of even the most complex formula fields. To calculate the field
result of a single field use the [Field.update()](./update/#default) method. To update fields in the whole document
use [Document.update_fields()](../../aspose.words/document/update_fields/#default).

You can get the plain text version of the field code using the [Field.get_field_code()](./get_field_code/#bool) method.
You can get and set the plain text version of the field result using the [Field.result](./result/) property.
Both the field code and field result can contain complex content, such as nested fields, paragraphs, shapes,
tables and in this case you might want to work with the field nodes directly if you need more control.

You do not create instances of the [Field](./) class directly.
To create a new field use the [DocumentBuilder.insert_field()](../../aspose.words/documentbuilder/insert_field/#str) method.




### Properties

| Name | Description |
| --- | --- |
| [display_result](./display_result/) | Gets the text that represents the displayed field result. |
| [end](./end/) | Gets the node that represents the field end. |
| [format](./format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [is_dirty](./is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [is_locked](./is_locked/) | Gets or sets whether the field is locked (should not recalculate its result). |
| [locale_id](./locale_id/) | Gets or sets the LCID of the field. |
| [result](./result/) | Gets or sets text that is between the field separator and field end. |
| [separator](./separator/) | Gets the node that represents the field separator. Can be null. |
| [start](./start/) | Gets the node that represents the start of the field. |
| [type](./type/) | Gets the Microsoft Word field type. |

### Methods

| Name | Description |
| --- | --- |
|[ as_field()](./as_field/#default) |  |
|[ as_field_add_in()](./as_field_add_in/#default) |  |
|[ as_field_address_block()](./as_field_address_block/#default) |  |
|[ as_field_advance()](./as_field_advance/#default) |  |
|[ as_field_ask()](./as_field_ask/#default) |  |
|[ as_field_author()](./as_field_author/#default) |  |
|[ as_field_auto_num()](./as_field_auto_num/#default) |  |
|[ as_field_auto_num_lgl()](./as_field_auto_num_lgl/#default) |  |
|[ as_field_auto_num_out()](./as_field_auto_num_out/#default) |  |
|[ as_field_auto_text()](./as_field_auto_text/#default) |  |
|[ as_field_auto_text_list()](./as_field_auto_text_list/#default) |  |
|[ as_field_barcode()](./as_field_barcode/#default) |  |
|[ as_field_bibliography()](./as_field_bibliography/#default) |  |
|[ as_field_bidi_outline()](./as_field_bidi_outline/#default) |  |
|[ as_field_citation()](./as_field_citation/#default) |  |
|[ as_field_comments()](./as_field_comments/#default) |  |
|[ as_field_compare()](./as_field_compare/#default) |  |
|[ as_field_create_date()](./as_field_create_date/#default) |  |
|[ as_field_data()](./as_field_data/#default) |  |
|[ as_field_database()](./as_field_database/#default) |  |
|[ as_field_date()](./as_field_date/#default) |  |
|[ as_field_dde()](./as_field_dde/#default) |  |
|[ as_field_dde_auto()](./as_field_dde_auto/#default) |  |
|[ as_field_display_barcode()](./as_field_display_barcode/#default) |  |
|[ as_field_doc_property()](./as_field_doc_property/#default) |  |
|[ as_field_doc_variable()](./as_field_doc_variable/#default) |  |
|[ as_field_edit_time()](./as_field_edit_time/#default) |  |
|[ as_field_embed()](./as_field_embed/#default) |  |
|[ as_field_eq()](./as_field_eq/#default) |  |
|[ as_field_file_name()](./as_field_file_name/#default) |  |
|[ as_field_file_size()](./as_field_file_size/#default) |  |
|[ as_field_fill_in()](./as_field_fill_in/#default) |  |
|[ as_field_footnote_ref()](./as_field_footnote_ref/#default) |  |
|[ as_field_form_check_box()](./as_field_form_check_box/#default) |  |
|[ as_field_form_drop_down()](./as_field_form_drop_down/#default) |  |
|[ as_field_form_text()](./as_field_form_text/#default) |  |
|[ as_field_formula()](./as_field_formula/#default) |  |
|[ as_field_glossary()](./as_field_glossary/#default) |  |
|[ as_field_go_to_button()](./as_field_go_to_button/#default) |  |
|[ as_field_greeting_line()](./as_field_greeting_line/#default) |  |
|[ as_field_hyperlink()](./as_field_hyperlink/#default) |  |
|[ as_field_if()](./as_field_if/#default) |  |
|[ as_field_import()](./as_field_import/#default) |  |
|[ as_field_include()](./as_field_include/#default) |  |
|[ as_field_include_picture()](./as_field_include_picture/#default) |  |
|[ as_field_include_text()](./as_field_include_text/#default) |  |
|[ as_field_index()](./as_field_index/#default) |  |
|[ as_field_info()](./as_field_info/#default) |  |
|[ as_field_keywords()](./as_field_keywords/#default) |  |
|[ as_field_last_saved_by()](./as_field_last_saved_by/#default) |  |
|[ as_field_link()](./as_field_link/#default) |  |
|[ as_field_list_num()](./as_field_list_num/#default) |  |
|[ as_field_macro_button()](./as_field_macro_button/#default) |  |
|[ as_field_merge_barcode()](./as_field_merge_barcode/#default) |  |
|[ as_field_merge_field()](./as_field_merge_field/#default) |  |
|[ as_field_merge_rec()](./as_field_merge_rec/#default) |  |
|[ as_field_merge_seq()](./as_field_merge_seq/#default) |  |
|[ as_field_next()](./as_field_next/#default) |  |
|[ as_field_next_if()](./as_field_next_if/#default) |  |
|[ as_field_note_ref()](./as_field_note_ref/#default) |  |
|[ as_field_num_chars()](./as_field_num_chars/#default) |  |
|[ as_field_num_pages()](./as_field_num_pages/#default) |  |
|[ as_field_num_words()](./as_field_num_words/#default) |  |
|[ as_field_ocx()](./as_field_ocx/#default) |  |
|[ as_field_page()](./as_field_page/#default) |  |
|[ as_field_page_ref()](./as_field_page_ref/#default) |  |
|[ as_field_print()](./as_field_print/#default) |  |
|[ as_field_print_date()](./as_field_print_date/#default) |  |
|[ as_field_private()](./as_field_private/#default) |  |
|[ as_field_quote()](./as_field_quote/#default) |  |
|[ as_field_rd()](./as_field_rd/#default) |  |
|[ as_field_ref()](./as_field_ref/#default) |  |
|[ as_field_rev_num()](./as_field_rev_num/#default) |  |
|[ as_field_save_date()](./as_field_save_date/#default) |  |
|[ as_field_section()](./as_field_section/#default) |  |
|[ as_field_section_pages()](./as_field_section_pages/#default) |  |
|[ as_field_seq()](./as_field_seq/#default) |  |
|[ as_field_set()](./as_field_set/#default) |  |
|[ as_field_shape()](./as_field_shape/#default) |  |
|[ as_field_skip_if()](./as_field_skip_if/#default) |  |
|[ as_field_style_ref()](./as_field_style_ref/#default) |  |
|[ as_field_subject()](./as_field_subject/#default) |  |
|[ as_field_symbol()](./as_field_symbol/#default) |  |
|[ as_field_ta()](./as_field_ta/#default) |  |
|[ as_field_tc()](./as_field_tc/#default) |  |
|[ as_field_template()](./as_field_template/#default) |  |
|[ as_field_time()](./as_field_time/#default) |  |
|[ as_field_title()](./as_field_title/#default) |  |
|[ as_field_toa()](./as_field_toa/#default) |  |
|[ as_field_toc()](./as_field_toc/#default) |  |
|[ as_field_unknown()](./as_field_unknown/#default) |  |
|[ as_field_user_address()](./as_field_user_address/#default) |  |
|[ as_field_user_initials()](./as_field_user_initials/#default) |  |
|[ as_field_user_name()](./as_field_user_name/#default) |  |
|[ as_field_xe()](./as_field_xe/#default) |  |
|[ get_field_code()](./get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
|[ get_field_code(include_child_field_codes)](./get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator). |
|[ remove()](./remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
|[ unlink()](./unlink/#default) | Performs the field unlink. |
|[ update()](./update/#default) | Performs the field update. Throws if the field is being updated already. |
|[ update(ignore_merge_format)](./update/#bool) | Performs a field update. Throws if the field is being updated already. |

### Examples

Shows how to insert a field into a document using a field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field("DATE \\@ \"dddd, MMMM dd, yyyy\"")

self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.get_field_code())

# This overload of the "insert_field" method automatically updates inserted fields.
self.assertAlmostEqual(datetime.strptime(field.result, "%A, %B %d, %Y"), datetime.now(), delta=timedelta(1))
```

### See Also

* module [aspose.words.fields](../)

