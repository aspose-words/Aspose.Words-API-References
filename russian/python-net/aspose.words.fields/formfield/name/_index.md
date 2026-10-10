---
title: FormField.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "FormField.name property. Gets or sets the form field name."
type: docs
weight: 130
url: /ru/python-net/aspose.words.fields/formfield/name/
---

## FormField.name property

Gets or sets the form field name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Microsoft Word allows strings with at most 20 characters.


### Examples

Shows how to insert a combo box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please select a fruit: ')
# Вставьте комбобокс, который позволит пользователю выбрать вариант из набора строк.
combo_box = builder.insert_combo_box('MyComboBox', ['Apple', 'Banana', 'Cherry'], 0)
self.assertEqual('MyComboBox', combo_box.name)
self.assertEqual(aw.fields.FieldType.FIELD_FORM_DROP_DOWN, combo_box.type)
self.assertEqual('Apple', combo_box.result)
# Поле формы будет отображаться в виде HTML‑тега "select".
doc.save(file_name=ARTIFACTS_DIR + 'FormFields.Create.html')
```

### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

