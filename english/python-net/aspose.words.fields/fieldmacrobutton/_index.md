---
title: FieldMacroButton class
linktitle: FieldMacroButton class
articleTitle: FieldMacroButton class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldMacroButton class. Implements the MACROBUTTON field"
type: docs
weight: 670
url: /python-net/aspose.words.fields/fieldmacrobutton/
---

## FieldMacroButton class

Implements the MACROBUTTON field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Allows a macro or command to be run.

In Aspose.Words this field can also act as a merge field.




**Inheritance:** [FieldMacroButton](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldMacroButton()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [display_text](./display_text/) | Gets or sets the text to appear as the "button" that is selected to run the macro or command. |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [macro_name](./macro_name/) | Gets or sets the name of the macro or command to run. |
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

Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking.

```python
doc = aw.Document(MY_DIR + 'Macro.docm')
builder = aw.DocumentBuilder(doc)
self.assertTrue(doc.has_macros)
# Insert a MACROBUTTON field, and reference one of the document's macros by name in the "macro_name" property.
field = builder.insert_field(aw.fields.FieldType.FIELD_MACRO_BUTTON, True).as_field_macro_button()
field.macro_name = 'MyMacro'
field.display_text = 'Double click to run macro: ' + field.macro_name
self.assertEqual(' MACROBUTTON  MyMacro Double click to run macro: MyMacro', field.get_field_code())
# Use the property to reference "ViewZoom200", a macro that ships with Microsoft Word.
# We can find all other macros via View -> Macros (dropdown) -> View Macros.
# In that menu, select "Word Commands" from the "Macros in:" drop down.
# If our document contains a custom macro with the same name as a stock macro,
# our macro will be the one that the MACROBUTTON field runs.
builder.insert_paragraph()
field = builder.insert_field(aw.fields.FieldType.FIELD_MACRO_BUTTON, True).as_field_macro_button()
field.macro_name = 'ViewZoom200'
field.display_text = 'Run ' + field.macro_name
self.assertEqual(' MACROBUTTON  ViewZoom200 Run ViewZoom200', field.get_field_code())
# Save the document as a macro-enabled document type.
doc.save(ARTIFACTS_DIR + 'Field.field_macro_button.docm')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

