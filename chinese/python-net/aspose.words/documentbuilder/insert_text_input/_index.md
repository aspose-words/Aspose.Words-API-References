---
title: DocumentBuilder.insert_text_input method
linktitle: insert_text_input method
articleTitle: insert_text_input method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_text_input method. Inserts a text form field at the current position."
type: docs
weight: 510
url: /zh/python-net/aspose.words/documentbuilder/insert_text_input/
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
# 插入一个表单，提示用户输入文本。
builder.insert_text_input('TextInput', aw.fields.TextFormFieldType.REGULAR, '', 'Enter your text here', 0)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTextInput.docx')
```

Shows how to create form fields.

```python
builder = aw.DocumentBuilder()
# 表单字段是文档中的对象，用户可以通过提示输入值与之交互。
# 我们可以使用文档生成器创建它们，下面有两种方法。
# 1 -  基本文本输入：
builder.insert_text_input('My text input', aw.fields.TextFormFieldType.REGULAR, '', 'Enter your name here', 30)
# 2 -  带提示文本的组合框，以及一系列可能的值：
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
# 插入一个文本输入字段，允许用户点击并输入文本。
# 分配一些占位符文本，用户可以覆盖并传递它
# 将最大文本长度设为 0，以对表单字段的内容不设限制。
builder.insert_text_input('TextInput1', aw.fields.TextFormFieldType.REGULAR, '', 'Placeholder text', 0)
# 表单字段将以 "input" HTML 标签的形式出现，类型为 "text"。
doc.save(file_name=ARTIFACTS_DIR + 'FormFields.TextInput.html')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

