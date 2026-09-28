---
title: Document.has_macros property
linktitle: has_macros property
articleTitle: has_macros property
second_title: Aspose.Words for Python
description: "Document.has_macros property. Returns ``True`` if the document has a VBA project (macros)."
type: docs
weight: 200
url: /de/python-net/aspose.words/document/has_macros/
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
# Fügen Sie ein MACROBUTTON-Feld ein und verweisen Sie im Property MacroName per Namen auf eines der Makros des Dokuments.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'MyMacro'
field.display_text = 'Double click to run macro: ' + field.macro_name
self.assertEqual(' MACROBUTTON  MyMacro Double click to run macro: MyMacro', field.get_field_code())
# Verwenden Sie die Eigenschaft, um "ViewZoom200" zu referenzieren, ein Makro, das mit Microsoft Word geliefert wird.
# Wir können alle anderen Makros über View -> Macros (dropdown) -> View Macros finden.
# Wählen Sie in diesem Menü "Word Commands" aus dem Dropdown "Macros in:" aus.
# Wenn unser Dokument ein benutzerdefiniertes Makro mit demselben Namen wie ein Standardmakro enthält,
# wird unser Makro dasjenige sein, das das MACROBUTTON-Feld ausführt.
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'ViewZoom200'
field.display_text = 'Run ' + field.macro_name
self.assertEqual(' MACROBUTTON  ViewZoom200 Run ViewZoom200', field.get_field_code())
# Speichern Sie das Dokument als makroaktivierten Dokumenttyp.
doc.save(file_name=ARTIFACTS_DIR + 'Field.MACROBUTTON.docm')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.remove_macros()](../remove_macros/#default)

