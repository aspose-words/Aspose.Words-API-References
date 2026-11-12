---
title: DropDownItemCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.remove method. Removes the specified value from the collection."
type: docs
weight: 80
url: /tr/python-net/aspose.words.fields/dropdownitemcollection/remove/
---

## remove(name) {#str}

Removes the specified value from the collection.


```python
def remove(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The case-sensitive value to remove. |

### Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR

class ExampleFormFields(ApiExampleBase):

    def test_drop_down_item_collection(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Bir combo kutusu ekleyin ve ardından açılır öğeler koleksiyonunu doğrulayın.
        # Microsoft Word'de kullanıcı combo kutusuna tıklayacak,
        # ve ardından koleksiyondaki metin öğelerinden birini görüntülemek için seçin.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Mevcut bir açılır kutu öğeleri koleksiyonuna yeni bir öğe eklemenin iki yolu vardır.
        # 1 - Bir öğeyi koleksiyonun sonuna ekleyin:
        drop_down_items.add('Four')
        # 2 - Belirtilen bir indeksde başka bir öğenin önüne bir öğe ekleyin:
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Koleksiyon üzerinde yineleme yapın ve her öğeyi yazdırın.
        for item in drop_down_items:
            print(item)
        # Açılır öğeler koleksiyonundan elemanları kaldırmanın iki yolu vardır.
        # 1 - Geçilen dizeye eşit içeriğe sahip bir öğeyi kaldırın:
        drop_down_items.remove('Four')
        # 2 - Bir indeksdeki öğeyi kaldırın:
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Açılır öğeler koleksiyonunun tamamını boşaltın.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

