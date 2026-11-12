---
title: FieldMacroButton.macro_name property
linktitle: macro_name property
articleTitle: macro_name property
second_title: Aspose.Words for Python
description: "FieldMacroButton.macro_name property. Gets or sets the name of the macro or command to run."
type: docs
weight: 30
url: /tr/python-net/aspose.words.fields/fieldmacrobutton/macro_name/
---

## FieldMacroButton.macro_name property

Gets or sets the name of the macro or command to run.


```python
@property
def macro_name(self) -> str:
    ...

@macro_name.setter
def macro_name(self, value: str):
    ...

```

### Examples

Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking.

```python
doc = aw.Document(file_name=MY_DIR + 'Macro.docm')
builder = aw.DocumentBuilder(doc=doc)
self.assertTrue(doc.has_macros)
# Bir MACROBUTTON alanı ekleyin ve MacroName özelliğinde belge makrolarından birine adını referans verin.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'MyMacro'
field.display_text = 'Double click to run macro: ' + field.macro_name
self.assertEqual(' MACROBUTTON  MyMacro Double click to run macro: MyMacro', field.get_field_code())
# Bu özelliği, Microsoft Word ile gelen "ViewZoom200" makrosuna referans vermek için kullanın.
# Tüm diğer makroları Görünüm -> Makrolar (açılır menü) -> Makroları Görüntüle yoluyla bulabiliriz.
# Bu menüde, "Macros in:" açılır menüsünden "Word Commands" seçeneğini seçin.
# Eğer belgemiz, yerleşik bir makro ile aynı ada sahip bir özel makro içeriyorsa,
# bizim makromuz, MACROBUTTON alanının çalıştırdığı makro olacaktır.
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'ViewZoom200'
field.display_text = 'Run ' + field.macro_name
self.assertEqual(' MACROBUTTON  ViewZoom200 Run ViewZoom200', field.get_field_code())
# Belgeyi makro etkin bir belge türü olarak kaydedin.
doc.save(file_name=ARTIFACTS_DIR + 'Field.MACROBUTTON.docm')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldMacroButton](../)

