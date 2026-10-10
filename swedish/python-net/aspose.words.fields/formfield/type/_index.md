---
title: FormField.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "FormField.type property. Returns the form field type."
type: docs
weight: 220
url: /sv/python-net/aspose.words.fields/formfield/type/
---

## FormField.type property

Returns the form field type.


```python
@property
def type(self) -> aspose.words.fields.FieldType:
    ...

```

### Examples

Shows how to insert a combo box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please select a fruit: ')
# Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
combo_box = builder.insert_combo_box('MyComboBox', ['Apple', 'Banana', 'Cherry'], 0)
self.assertEqual('MyComboBox', combo_box.name)
self.assertEqual(aw.fields.FieldType.FIELD_FORM_DROP_DOWN, combo_box.type)
self.assertEqual('Apple', combo_box.result)
# Formulärfältet kommer att visas i form av en "select"-html-tagg.
doc.save(file_name=ARTIFACTS_DIR + 'FormFields.Create.html')
```

### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

