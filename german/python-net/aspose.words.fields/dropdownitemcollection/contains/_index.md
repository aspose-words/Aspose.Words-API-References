---
title: DropDownItemCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.contains method. Determines whether the collection contains the specified value."
type: docs
weight: 50
url: /de/python-net/aspose.words.fields/dropdownitemcollection/contains/
---

## contains(value) {#str}

Determines whether the collection contains the specified value.


```python
def contains(self, value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | str | Case-sensitive value to locate. |

### Returns

``True`` if the item is found in the collection; otherwise, ``False``.


### Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR

class ExampleFormFields(ApiExampleBase):

    def test_drop_down_item_collection(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Fügen Sie ein Kombinationsfeld ein und überprüfen Sie anschließend dessen Sammlung von Dropdown‑Einträgen.
        # In Microsoft Word wird der Benutzer das Kombinationsfeld anklicken,
        # und dann wählen Sie eines der Textelemente in der Sammlung zur Anzeige aus.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Es gibt zwei Möglichkeiten, ein neues Element zu einer bestehenden Sammlung von Dropdown-Box-Elementen hinzuzufügen.
        # 1 - Ein Element am Ende der Sammlung anhängen:
        drop_down_items.add('Four')
        # 2 - Ein Element vor einem anderen Element an einem angegebenen Index einfügen:
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Durchlaufen Sie die Sammlung und geben jedes Element aus.
        for item in drop_down_items:
            print(item)
        # Es gibt zwei Möglichkeiten, Elemente aus einer Sammlung von Dropdown-Elementen zu entfernen.
        # 1 - Ein Element entfernen, dessen Inhalt dem übergebenen String entspricht:
        drop_down_items.remove('Four')
        # 2 - Ein Element an einem Index entfernen:
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Leeren Sie die gesamte Sammlung von Dropdown-Elementen.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

