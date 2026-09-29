---
title: Document.has_macros property
linktitle: has_macros property
articleTitle: has_macros property
second_title: Aspose.Words for Python
description: "Document.has_macros property. Returns ``True`` if the document has a VBA project (macros)."
type: docs
weight: 200
url: /ru/python-net/aspose.words/document/has_macros/
---

## Document.has_macros property

Returns ``True`` if the document has a VBA project (macros).



```python
@property
def has_macros(self) -> bool:
    ...

```

### Examples

Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking.

```python
doc = aw.Document(file_name=MY_DIR + 'Macro.docm')
builder = aw.DocumentBuilder(doc=doc)
self.assertTrue(doc.has_macros)
# Вставьте поле MACROBUTTON и укажите одну из макросов документа по имени в свойстве MacroName.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'MyMacro'
field.display_text = 'Double click to run macro: ' + field.macro_name
self.assertEqual(' MACROBUTTON  MyMacro Double click to run macro: MyMacro', field.get_field_code())
# Используйте свойство, чтобы сослаться на "ViewZoom200", макрос, поставляемый с Microsoft Word.
# Все остальные макросы можно найти через View -> Macros (выпадающий список) -> View Macros.
# В этом меню выберите "Word Commands" в выпадающем списке "Macros in:".
# Если наш документ содержит пользовательский макрос с тем же именем, что и штатный макрос,
# наш макрос будет тем, который запускает поле MACROBUTTON.
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'ViewZoom200'
field.display_text = 'Run ' + field.macro_name
self.assertEqual(' MACROBUTTON  ViewZoom200 Run ViewZoom200', field.get_field_code())
# Сохраните документ в формате, поддерживающем макросы.
doc.save(file_name=ARTIFACTS_DIR + 'Field.MACROBUTTON.docm')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.remove_macros()](../remove_macros/#default)

