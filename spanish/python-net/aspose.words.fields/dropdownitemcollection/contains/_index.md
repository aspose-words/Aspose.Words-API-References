---
title: DropDownItemCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.contains method. Determines whether the collection contains the specified value."
type: docs
weight: 50
url: /es/python-net/aspose.words.fields/dropdownitemcollection/contains/
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
        # Inserte un cuadro combinado y luego verifique su colección de elementos desplegables.
        # En Microsoft Word, el usuario hará clic en el cuadro combinado,
        # y luego elija uno de los elementos de texto en la colección para mostrar.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Hay dos formas de agregar un nuevo elemento a una colección existente de elementos de cuadro desplegable.
        # 1 - Añadir un elemento al final de la colección:
        drop_down_items.add('Four')
        # 2 - Insertar un elemento antes de otro en un índice especificado:
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Iterar sobre la colección e imprimir cada elemento.
        for item in drop_down_items:
            print(item)
        # Hay dos formas de eliminar elementos de una colección de elementos desplegables.
        # 1 - Eliminar un elemento cuyo contenido sea igual a la cadena pasada:
        drop_down_items.remove('Four')
        # 2 - Eliminar un elemento en un índice:
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Vaciar toda la colección de elementos desplegables.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

