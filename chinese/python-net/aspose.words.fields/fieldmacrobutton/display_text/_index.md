---
title: FieldMacroButton.display_text property
linktitle: display_text property
articleTitle: display_text property
second_title: Aspose.Words for Python
description: "FieldMacroButton.display_text property. Gets or sets the text to appear as the button that is selected to run the macro or command."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldmacrobutton/display_text/
---

## FieldMacroButton.display_text property

Gets or sets the text to appear as the "button" that is selected to run the macro or command.


```python
@property
def display_text(self) -> str:
    ...

@display_text.setter
def display_text(self, value: str):
    ...

```

### Examples

Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking.

```python
doc = aw.Document(file_name=MY_DIR + 'Macro.docm')
builder = aw.DocumentBuilder(doc=doc)
self.assertTrue(doc.has_macros)
# 插入一个 MACROBUTTON 字段，并在 MacroName 属性中按名称引用文档的宏之一。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'MyMacro'
field.display_text = 'Double click to run macro: ' + field.macro_name
self.assertEqual(' MACROBUTTON  MyMacro Double click to run macro: MyMacro', field.get_field_code())
# 使用该属性引用 "ViewZoom200"，这是随 Microsoft Word 附带的宏。
# 我们可以通过 View -> Macros（下拉）-> View Macros 找到所有其他宏。
# 在该菜单中，从 "Macros in:" 下拉列表中选择 "Word Commands"。
# 如果我们的文档包含一个与内置宏同名的自定义宏，
# 我们的宏将是 MACROBUTTON 字段运行的宏。
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'ViewZoom200'
field.display_text = 'Run ' + field.macro_name
self.assertEqual(' MACROBUTTON  ViewZoom200 Run ViewZoom200', field.get_field_code())
# 将文档另存为启用宏的文档类型。
doc.save(file_name=ARTIFACTS_DIR + 'Field.MACROBUTTON.docm')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldMacroButton](../)

