---
title: FieldMacroButton.macro_name property
linktitle: macro_name property
articleTitle: macro_name property
second_title: Aspose.Words for Python
description: "FieldMacroButton.macro_name property. Gets or sets the name of the macro or command to run."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldmacrobutton/macro_name/
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
# Insérez un champ MACROBUTTON et faites référence à l'une des macros du document par son nom dans la propriété MacroName.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'MyMacro'
field.display_text = 'Double click to run macro: ' + field.macro_name
self.assertEqual(' MACROBUTTON  MyMacro Double click to run macro: MyMacro', field.get_field_code())
# Utilisez la propriété pour faire référence à "ViewZoom200", une macro fournie avec Microsoft Word.
# Nous pouvons trouver toutes les autres macros via Affichage -> Macros (menu déroulant) -> Afficher les macros.
# Dans ce menu, sélectionnez "Commandes Word" dans la liste déroulante "Macros dans :".
# Si notre document contient une macro personnalisée portant le même nom qu'une macro standard,
# cette macro sera celle que le champ MACROBUTTON exécutera.
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MACRO_BUTTON, update_field=True).as_field_macro_button()
field.macro_name = 'ViewZoom200'
field.display_text = 'Run ' + field.macro_name
self.assertEqual(' MACROBUTTON  ViewZoom200 Run ViewZoom200', field.get_field_code())
# Enregistrez le document en tant que type de document activé par macro.
doc.save(file_name=ARTIFACTS_DIR + 'Field.MACROBUTTON.docm')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldMacroButton](../)

