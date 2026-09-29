---
title: DropDownItemCollection.index_of method
linktitle: index_of method
articleTitle: index_of method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.index_of method. Returns the zero-based index of the specified value in the collection."
type: docs
weight: 60
url: /ru/python-net/aspose.words.fields/dropdownitemcollection/index_of/
---

## index_of(value) {#str}

Returns the zero-based index of the specified value in the collection.


```python
def index_of(self, value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | str | The case-sensitive value to locate. |

### Returns

The zero based index. Negative value if not found.


### Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR

class ExampleFormFields(ApiExampleBase):

    def test_drop_down_item_collection(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Вставьте комбинированный список, а затем проверьте его коллекцию элементов выпадающего списка.
        # В Microsoft Word пользователь щёлкнет по комбинированному списку,
        # а затем выберите один из элементов текста в коллекции для отображения.
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # Существует два способа добавить новый элемент в существующую коллекцию элементов выпадающего списка.
        # 1 - Добавить элемент в конец коллекции:
        drop_down_items.add('Four')
        # 2 - Вставить элемент перед другим элементом по указанному индексу:
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # Итерировать по коллекции и вывести каждый элемент.
        for item in drop_down_items:
            print(item)
        # Существует два способа удаления элементов из коллекции выпадающих элементов.
        # 1 - Удалить элемент, содержимое которого равно переданной строке:
        drop_down_items.remove('Four')
        # 2 - Удалить элемент по индексу:
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # Очистить всю коллекцию выпадающих элементов.
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

