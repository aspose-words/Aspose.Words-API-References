---
title: DocumentBuilder.insert_text_input method
linktitle: insert_text_input method
articleTitle: insert_text_input method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_text_input method. Inserts a text form field at the current position."
type: docs
weight: 510
url: /ru/python-net/aspose.words/documentbuilder/insert_text_input/
---

## insert_text_input(name, type, format, field_value, max_length) {#str_textformfieldtype_str_str_int}

Inserts a text form field at the current position.


```python
def insert_text_input(self, name: str, type: aspose.words.fields.TextFormFieldType, format: str, field_value: str, max_length: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the form field. Can be an empty string. |
| type | [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/) | Specifies the type of the text form field. |
| format | str | Format string used to format the value of the form field. |
| field_value | str | Text that will be shown in the field. |
| max_length | int | Maximum length the user can enter into the form field. Set to zero for unlimited length. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


### Examples

Shows how to insert a text input form field into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте форму, которая предлагает пользователю ввести текст.
builder.insert_text_input('TextInput', aw.fields.TextFormFieldType.REGULAR, '', 'Enter your text here', 0)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTextInput.docx')
```

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

Shows how to insert a text input form field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text here: ')
# Вставьте текстовое поле ввода, которое позволит пользователю щёлкнуть по нему и ввести текст.
# Назначьте некоторый заполнитель текста, который пользователь может перезаписать и передать
# максимальная длина текста 0, чтобы не ограничивать содержимое поля формы.
builder.insert_text_input('TextInput1', aw.fields.TextFormFieldType.REGULAR, '', 'Placeholder text', 0)
# Поле формы будет отображаться в виде HTML‑тега "input" с типом "text".
doc.save(file_name=ARTIFACTS_DIR + 'FormFields.TextInput.html')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

