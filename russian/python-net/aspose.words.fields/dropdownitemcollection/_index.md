---
title: DropDownItemCollection class
linktitle: DropDownItemCollection class
articleTitle: DropDownItemCollection class
second_title: Aspose.Words for Python
description: "aspose.words.fields.DropDownItemCollection class. A collection of strings that represent all the items in a drop-down form field"
type: docs
weight: 40
url: /ru/python-net/aspose.words.fields/dropdownitemcollection/
---

## DropDownItemCollection class

A collection of strings that represent all the items in a drop-down form field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets the element at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(value)](./add/#str) | Adds a string to the end of the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ contains(value)](./contains/#str) | Determines whether the collection contains the specified value. |
|[ index_of(value)](./index_of/#str) | Returns the zero-based index of the specified value in the collection. |
|[ insert(index, value)](./insert/#int_str) | Inserts a string into the collection at the specified index. |
|[ remove(name)](./remove/#str) | Removes the specified value from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a value at the specified index. |

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

* module [aspose.words.fields](../)
* class [FormField](../formfield/)
* property [FormField.drop_down_items](../formfield/drop_down_items/)

