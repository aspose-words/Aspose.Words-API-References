---
title: TextFormFieldType enumeration
linktitle: TextFormFieldType enumeration
articleTitle: TextFormFieldType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fields.TextFormFieldType enumeration. Specifies the type of a text form field."
type: docs
weight: 1310
url: /ru/python-net/aspose.words.fields/textformfieldtype/
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
# Поля формы — это объекты в документе, с которыми пользователь может взаимодействовать, получая запрос ввести значения.
# Мы можем создать их, используя конструктор документов, а ниже приведены два способа сделать это.
# 1 -  Базовый ввод текста:
builder.insert_text_input('My text input', aw.fields.TextFormFieldType.REGULAR, '', 'Enter your name here', 30)
# 2 -  Выпадающий список с подсказкой и диапазоном возможных значений:
items = ['-- Select your favorite footwear --', 'Sneakers', 'Oxfords', 'Flip-flops', 'Other']
builder.insert_paragraph()
builder.insert_combo_box('My combo box', items, 0)
builder.document.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateForm.docx')
```

### See Also

* module [aspose.words.fields](../)

