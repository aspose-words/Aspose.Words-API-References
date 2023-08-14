---
title: TextFormFieldType enumeration
linktitle: TextFormFieldType enumeration
articleTitle: TextFormFieldType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fields.TextFormFieldType enumeration. Specifies the type of a text form field."
type: docs
weight: 1310
url: /python-net/aspose.words.fields/textformfieldtype/
---

## TextFormFieldType enumeration

Specifies the type of a text form field.


### Members

| Name | Description |
| --- | --- |
| REGULAR | The text form field can contain any text. |
| NUMBER | The text form field can contain only numbers. |
| DATE | The text form field can contain only a valid date value. |
| CURRENT_DATE | The text form field value is the current date when the field is updated. |
| CURRENT_TIME | The text form field value is the current time when the field is updated. |
| CALCULATED | The text form field value is calculated from the expression specified in the [FormField.text_input_default](../formfield/text_input_default/) property. |

### Examples

Shows how to create form fields.

```python
builder = aw.DocumentBuilder()

# Form fields are objects in the document that the user can interact with by being prompted to enter values.
# We can create them using a document builder, and below are two ways of doing so.
# 1 -  Basic text input:
builder.insert_text_input("My text input", aw.fields.TextFormFieldType.REGULAR,
    "", "Enter your name here", 30)

# 2 -  Combo box with prompt text, and a range of possible values:
items = [ "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other" ]

builder.insert_paragraph()
builder.insert_combo_box("My combo box", items, 0)

builder.document.save(ARTIFACTS_DIR + "DocumentBuilder.create_form.docx")
```

### See Also

* module [aspose.words.fields](../)

