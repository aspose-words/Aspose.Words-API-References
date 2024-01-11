---
title: Document.has_macros property
linktitle: has_macros property
articleTitle: has_macros property
second_title: Aspose.Words for Python
description: "Document.has_macros property. Returns ``True`` if the document has a VBA project (macros)."
type: docs
weight: 200
url: /python-net/aspose.words/document/has_macros/
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
doc = aw.Document(MY_DIR + "Macro.docm")
builder = aw.DocumentBuilder(doc)

self.assertTrue(doc.has_macros)

# Insert a MACROBUTTON field, and reference one of the document's macros by name in the "macro_name" property.
field = builder.insert_field(aw.fields.FieldType.FIELD_MACRO_BUTTON, True).as_field_macro_button()
field.macro_name = "MyMacro"
field.display_text = "Double click to run macro: " + field.macro_name

self.assertEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.get_field_code())

# Use the property to reference "ViewZoom200", a macro that ships with Microsoft Word.
# We can find all other macros via View -> Macros (dropdown) -> View Macros.
# In that menu, select "Word Commands" from the "Macros in:" drop down.
# If our document contains a custom macro with the same name as a stock macro,
# our macro will be the one that the MACROBUTTON field runs.
builder.insert_paragraph()
field = builder.insert_field(aw.fields.FieldType.FIELD_MACRO_BUTTON, True).as_field_macro_button()
field.macro_name = "ViewZoom200"
field.display_text = "Run " + field.macro_name

self.assertEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.get_field_code())

# Save the document as a macro-enabled document type.
doc.save(ARTIFACTS_DIR + "Field.field_macro_button.docm")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.remove_macros()](../remove_macros/#default)

