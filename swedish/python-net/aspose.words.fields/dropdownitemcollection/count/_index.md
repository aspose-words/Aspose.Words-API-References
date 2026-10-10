---
title: DropDownItemCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "DropDownItemCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/dropdownitemcollection/count/
---

## DropDownItemCollection.count property

Gets the number of elements contained in the collection.


```python
@property
def count(self) -> int:
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
        # Infoga en kombinationsruta och verifiera sedan dess samling av rullgardinsalternativ.
        # I Microsoft Word kommer användaren att klicka på kombinationsrutan,
        # och välj sedan ett av textobjekten i samlingen för att visa.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Det finns två sätt att lägga till ett nytt objekt i en befintlig samling av rullgardinsmenyobjekt.
        # 1 - Lägg till ett objekt i slutet av samlingen:
        drop_down_items.add('Four')
        # 2 - Infoga ett objekt före ett annat objekt på ett angivet index:
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Iterera över samlingen och skriv ut varje element.
        for item in drop_down_items:
            print(item)
        # Det finns två sätt att ta bort element från en samling av rullgardinsobjekt.
        # 1 - Ta bort ett objekt med innehåll som är lika med den överförda strängen:
        drop_down_items.remove('Four')
        # 2 - Ta bort ett objekt på ett index:
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Töm hela samlingen av rullgardinsobjekt.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

