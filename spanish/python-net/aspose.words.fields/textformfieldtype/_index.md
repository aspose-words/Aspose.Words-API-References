---
title: TextFormFieldType enumeration
linktitle: TextFormFieldType enumeration
articleTitle: TextFormFieldType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fields.TextFormFieldType enumeration. Specifies the type of a text form field."
type: docs
weight: 1310
url: /es/python-net/aspose.words.fields/textformfieldtype/
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
# Los campos de formulario son objetos en el documento con los que el usuario puede interactuar mediante una solicitud para ingresar valores.
# Podemos crearlos usando un generador de documentos, y a continuación se presentan dos formas de hacerlo.
# 1 -  Entrada de texto básica:
builder.insert_text_input('My text input', aw.fields.TextFormFieldType.REGULAR, '', 'Enter your name here', 30)
# 2 -  Cuadro combinado con texto de solicitud y un rango de valores posibles:
items = ['-- Select your favorite footwear --', 'Sneakers', 'Oxfords', 'Flip-flops', 'Other']
builder.insert_paragraph()
builder.insert_combo_box('My combo box', items, 0)
builder.document.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateForm.docx')
```

### See Also

* module [aspose.words.fields](../)

