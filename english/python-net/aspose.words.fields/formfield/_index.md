---
title: FormField class
linktitle: FormField class
articleTitle: FormField class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FormField class. Represents a single form field"
type: docs
weight: 1160
url: /python-net/aspose.words.fields/formfield/
---

## FormField class

Represents a single form field.
To learn more, visit the [Working with Form Fields](https://docs.aspose.com/words/python-net/working-with-form-fields/) documentation article.




### Remarks

Microsoft Word provides the following form fields: checkbox, text input and dropdown (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and
positioned as a character within a line of text.

A complete form field in a Word document is a complex structure represented by several
nodes: field start, field code such as FORMTEXT, form field data, field separator,
field result, field end and a bookmark. To programmatically create form fields in a Word document use
[DocumentBuilder.insert_check_box()](../../aspose.words/documentbuilder/insert_check_box/#str_bool_int),
[DocumentBuilder.insert_text_input()](../../aspose.words/documentbuilder/insert_text_input/#str_textformfieldtype_str_str_int) and
[DocumentBuilder.insert_combo_box()](../../aspose.words/documentbuilder/insert_combo_box/#str_strlist_int) which
make sure all of the form field nodes are created in a correct order and in a suitable state.




**Inheritance:** [FormField](./) → [SpecialChar](../../aspose.words/specialchar/) → [Inline](../../aspose.words/inline/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [calculate_on_exit](./calculate_on_exit/) | True if references to the specified form field are automatically updated whenever the field is exited. |
| [check_box_size](./check_box_size/) | Gets or sets the size of the checkbox in points. Has effect only when [FormField.is_check_box_exact_size](./is_check_box_exact_size/) is ``True``. |
| [checked](./checked/) | Gets or sets the checked status of the check box form field. Default value for this property is ``False``. |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [default](./default/) | Gets or sets the default value of the check box form field. Default value for this property is ``False``. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [drop_down_items](./drop_down_items/) | Provides access to the items of a dropdown form field. |
| [drop_down_selected_index](./drop_down_selected_index/) | Gets or sets the index specifying the currently selected item in a dropdown form field. |
| [enabled](./enabled/) | True if a form field is enabled. |
| [entry_macro](./entry_macro/) | Returns or sets an entry macro name for the form field. |
| [exit_macro](./exit_macro/) | Returns or sets an exit macro name for the form field. |
| [font](../../aspose.words/inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [help_text](./help_text/) | Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1. |
| [is_check_box_exact_size](./is_check_box_exact_size/) | Gets or sets the boolean value that indicates whether the size of the textbox is automatic or specified explicitly. |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_delete_revision](../../aspose.words/inline/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_format_revision](../../aspose.words/inline/is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_insert_revision](../../aspose.words/inline/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_move_from_revision](../../aspose.words/inline/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [is_move_to_revision](../../aspose.words/inline/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [max_length](./max_length/) | Maximum length for the text field. Zero when the length is not limited. |
| [name](./name/) | Gets or sets the form field name. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.FORM_FIELD](../../aspose.words/nodetype/#FORM_FIELD). |
| [own_help](./own_help/) | Specifies the source of the text that's displayed in a message box when a form field has the focus and the user presses F1. |
| [own_status](./own_status/) | Specifies the source of the text that's displayed in the status bar when a form field has the focus. |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](../../aspose.words/inline/parent_paragraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node.<br>(Inherited from [Inline](../../aspose.words/inline/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [result](./result/) | Gets or sets a string that represents the result of this form field. |
| [status_text](./status_text/) | Returns or sets the text that's displayed in the status bar when a form field has the focus. |
| [text_input_default](./text_input_default/) | Gets or sets the default string or a calculation expression of a text form field. |
| [text_input_format](./text_input_format/) | Returns or sets the text formatting for a text form field. |
| [text_input_type](./text_input_type/) | Gets or sets the type of a text form field. |
| [type](./type/) | Returns the form field type. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_field()](./remove_field/#default) | Removes the complete form field, not just the form field special character. |
|[ set_text_input_value(new_value)](./set_text_input_value/#object) | Applies the text format specified in [FormField.text_input_format](./text_input_format/) and stores the value in [FormField.result](./result/). |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to insert a combo box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please select a fruit: ')
# Insert a combo box which will allow a user to choose an option from a collection of strings.
combo_box = builder.insert_combo_box('MyComboBox', ['Apple', 'Banana', 'Cherry'], 0)
self.assertEqual('MyComboBox', combo_box.name)
self.assertEqual(aw.fields.FieldType.FIELD_FORM_DROP_DOWN, combo_box.type)
self.assertEqual('Apple', combo_box.result)
# The form field will appear in the form of a "select" html tag.
doc.save(file_name=ARTIFACTS_DIR + 'FormFields.Create.html')
```

Shows how to formatting the entire FormField, including the field value.

```python
doc = aw.Document(MY_DIR + 'Form fields.docx')
form_field = doc.range.form_fields[0]
form_field.font.bold = True
form_field.font.size = 24
form_field.font.color = aspose.pydrawing.Color.red
form_field.result = 'Aspose.FormField'
doc = DocumentHelper.save_open(doc)
form_field_run = doc.first_section.body.first_paragraph.runs[1]
self.assertEqual('Aspose.FormField', form_field_run.text)
self.assertEqual(True, form_field_run.font.bold)
self.assertEqual(24, form_field_run.font.size)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), form_field_run.font.color.to_argb())
```

### See Also

* module [aspose.words.fields](../)
* class [SpecialChar](../../aspose.words/specialchar/)

