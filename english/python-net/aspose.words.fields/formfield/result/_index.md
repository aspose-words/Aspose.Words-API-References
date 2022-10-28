---
title: result property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a string that represents the result of this form field."
type: docs
weight: 170
url: /python-net/aspose.words.fields/formfield/result/
---

## FormField.result property

Gets or sets a string that represents the result of this form field.

For a text form field the result is the text that is in the field.

For a checkbox form field the result can be "1" or "0" to indicate checked or unchecked.

For a dropdown form field the result is the string selected in the dropdown.

Setting [FormField.result](./) for a text form field does not apply the text format
specified in [FormField.text_input_format](../text_input_format/). If you want to set a value and apply the
format, use the [FormField.set_text_input_value()](../set_text_input_value/#object) method.

For a text form field the [FormField.text_input_default](../text_input_default/) value is applied
if  is``None``.




### Examples

Shows how to insert a combo box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Please select a fruit: ")

# Insert a combo box which will allow a user to choose an option from a collection of strings.
combo_box = builder.insert_combo_box("MyComboBox", ["Apple", "Banana", "Cherry"], 0)

self.assertEqual("MyComboBox", combo_box.name)
self.assertEqual(aw.fields.FieldType.FIELD_FORM_DROP_DOWN, combo_box.type)
self.assertEqual("Apple", combo_box.result)

# The form field will appear in the form of a "select" html tag.
doc.save(ARTIFACTS_DIR + "FormFields.create.html")
```

### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

