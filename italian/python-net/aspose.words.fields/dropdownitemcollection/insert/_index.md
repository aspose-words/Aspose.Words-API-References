---
title: DropDownItemCollection.insert method
linktitle: insert method
articleTitle: insert method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.insert method. Inserts a string into the collection at the specified index."
type: docs
weight: 70
url: /it/python-net/aspose.words.fields/dropdownitemcollection/insert/
---

## insert(index, value) {#int_str}

Inserts a string into the collection at the specified index.


```python
def insert(self, index: int, value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index at which value is inserted. |
| value | str | The string to insert. |

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

