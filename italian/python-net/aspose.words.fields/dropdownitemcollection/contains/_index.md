---
title: DropDownItemCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.contains method. Determines whether the collection contains the specified value."
type: docs
weight: 50
url: /it/python-net/aspose.words.fields/dropdownitemcollection/contains/
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
        # Inserisci una casella combinata, quindi verifica la sua raccolta di elementi a discesa.
        # In Microsoft Word, l'utente farà clic sulla casella combinata,
        # e poi scegli uno degli elementi di testo nella collezione da visualizzare.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Ci sono due modi per aggiungere un nuovo elemento a una collezione esistente di voci di casella a discesa.
        # 1 - Aggiungi un elemento alla fine della collezione:
        drop_down_items.add('Four')
        # 2 - Inserisci un elemento prima di un altro elemento a un indice specificato:
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Itera sulla collezione e stampa ogni elemento.
        for item in drop_down_items:
            print(item)
        # Ci sono due modi per rimuovere elementi da una collezione di voci a discesa.
        # 1 - Rimuovi un elemento il cui contenuto è uguale alla stringa fornita:
        drop_down_items.remove('Four')
        # 2 - Rimuovi un elemento a un indice:
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Svuota l'intera collezione di voci a discesa.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

