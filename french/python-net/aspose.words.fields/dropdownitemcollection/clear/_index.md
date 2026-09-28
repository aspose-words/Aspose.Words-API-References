---
title: DropDownItemCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.clear method. Removes all elements from the collection."
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/dropdownitemcollection/clear/
---

## clear() {#default}

Removes all elements from the collection.


```python
def clear(self):
    ...
```

### Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR

class ExampleFormFields(ApiExampleBase):

    def test_drop_down_item_collection(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Insérez une zone combinée, puis vérifiez sa collection d'éléments déroulants.
        # Dans Microsoft Word, l'utilisateur cliquera sur la zone combinée,
        # et ensuite choisissez l'un des éléments de texte dans la collection à afficher.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Il existe deux façons d'ajouter un nouvel élément à une collection existante d'éléments de boîte déroulante.
        # 1 - Ajouter un élément à la fin de la collection :
        drop_down_items.add('Four')
        # 2 - Insérer un élément avant un autre élément à un indice spécifié :
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Itérez sur la collection et affichez chaque élément.
        for item in drop_down_items:
            print(item)
        # Il existe deux façons de supprimer des éléments d'une collection d'éléments déroulants.
        # 1 - Supprimer un élément dont le contenu est égal à la chaîne passée :
        drop_down_items.remove('Four')
        # 2 - Supprimer un élément à un indice :
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Videz toute la collection d'éléments déroulants.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

