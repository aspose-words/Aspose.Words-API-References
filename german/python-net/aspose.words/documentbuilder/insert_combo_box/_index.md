---
title: DocumentBuilder.insert_combo_box method
linktitle: insert_combo_box method
articleTitle: insert_combo_box method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_combo_box method. Inserts a combobox form field at the current position."
type: docs
weight: 300
url: /de/python-net/aspose.words/documentbuilder/insert_combo_box/
---

## insert_combo_box(name, items, selected_index) {#str_strlist_int}

Inserts a combobox form field at the current position.


```python
def insert_combo_box(self, name: str, items: List[str], selected_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| items | List[str] | The items of the ComboBox. Maximum is 25 items. |
| selected_index | int | The index of the selected item in the ComboBox. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


### Examples

Shows how to create form fields.

```python
builder = aw.DocumentBuilder()
# Formularfelder sind Objekte im Dokument, mit denen der Benutzer interagieren kann, indem er aufgefordert wird, Werte einzugeben.
# Wir können sie mit einem document builder erstellen, und unten sind zwei Möglichkeiten, dies zu tun.
# 1 -  Einfache Texteingabe:
builder.insert_text_input('My text input', aw.fields.TextFormFieldType.REGULAR, '', 'Enter your name here', 30)
# 2 -  Kombinationsfeld mit Hinweistext und einer Reihe möglicher Werte:
items = ['-- Select your favorite footwear --', 'Sneakers', 'Oxfords', 'Flip-flops', 'Other']
builder.insert_paragraph()
builder.insert_combo_box('My combo box', items, 0)
builder.document.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateForm.docx')
```

Shows how to insert a combo box form field into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein Formular ein, das den Benutzer auffordert, einen der Einträge aus dem Menü auszuwählen.
builder.write('Pick a fruit: ')
items = ['Apple', 'Banana', 'Cherry']
builder.insert_combo_box('DropDown', items, 0)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertComboBox.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

