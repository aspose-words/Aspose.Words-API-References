---
title: DocumentBuilder.insert_check_box method
linktitle: insert_check_box method
articleTitle: insert_check_box method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_check_box method"
type: docs
weight: 290
url: /fr/python-net/aspose.words/documentbuilder/insert_check_box/
---

## insert_check_box(name, checked_value, size) {#str_bool_int}

Inserts a checkbox form field at the current position.


```python
def insert_check_box(self, name: str, checked_value: bool, size: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| checked_value | bool | Checked status of the checkbox form field. |
| size | int | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


## insert_check_box(name, default_value, checked_value, size) {#str_bool_bool_int}

Inserts a checkbox form field at the current position.


```python
def insert_check_box(self, name: str, default_value: bool, checked_value: bool, size: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| default_value | bool | Default value of the checkbox form field. |
| checked_value | bool | Current checked status of the checkbox form field. |
| size | int | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


## Examples

Shows how to insert checkboxes into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez des cases à cocher de tailles variables et d'états cochés par défaut.
builder.write('Unchecked check box of a default size: ')
builder.insert_check_box(name='', default_value=False, checked_value=False, size=0)
builder.insert_paragraph()
builder.write('Large checked check box: ')
builder.insert_check_box(name='CheckBox_Default', default_value=True, checked_value=True, size=50)
builder.insert_paragraph()
# Les champs de formulaire ont une limite de longueur de nom de 20 caractères.
builder.write('Very large checked check box: ')
builder.insert_check_box(name='CheckBox_OnlyCheckedValue', checked_value=True, size=100)
self.assertEqual('CheckBox_OnlyChecked', doc.range.form_fields[2].name)
# Nous pouvons interagir avec ces cases à cocher dans Microsoft Word en double-cliquant dessus.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertCheckBox.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

