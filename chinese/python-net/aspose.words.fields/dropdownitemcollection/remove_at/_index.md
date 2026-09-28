---
title: DropDownItemCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "DropDownItemCollection.remove_at method. Removes a value at the specified index."
type: docs
weight: 90
url: /zh/python-net/aspose.words.fields/dropdownitemcollection/remove_at/
---

## remove_at(index) {#int}

Removes a value at the specified index.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR

class ExampleFormFields(ApiExampleBase):

    def test_drop_down_item_collection(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # 插入一个组合框，然后验证其下拉项集合。
        # 在 Microsoft Word 中，用户将单击组合框，
        # 然后从集合中的文本项中选择一个进行显示。
        items = ['One', 'Two', 'Three']
        combo_box_field = builder.insert_combo_box('DropDown', items, 0)
        drop_down_items = combo_box_field.drop_down_items
        self.assertEqual(3, drop_down_items.count)
        self.assertEqual('One', drop_down_items[0])
        self.assertEqual(1, drop_down_items.index_of('Two'))
        self.assertTrue(drop_down_items.contains('Three'))
        # 有两种方法可以向现有的下拉框项集合中添加新项。
        # 1 - 将项追加到集合的末尾：
        drop_down_items.add('Four')
        # 2 - 在指定索引处将项插入到另一个项之前：
        drop_down_items.insert(3, 'Three and a half')
        self.assertEqual(5, drop_down_items.count)
        # 遍历集合并打印每个元素。
        for item in drop_down_items:
            print(item)
        # 有两种方法可以从下拉项集合中移除元素。
        # 1 - 移除内容等于给定字符串的项：
        drop_down_items.remove('Four')
        # 2 - 按索引移除项：
        drop_down_items.remove_at(3)
        self.assertEqual(3, drop_down_items.count)
        self.assertFalse(drop_down_items.contains('Three and a half'))
        self.assertFalse(drop_down_items.contains('Four'))
        doc.save(file_name=ARTIFACTS_DIR + 'FormFields.DropDownItemCollection.html')
        # 清空整个下拉项集合。
        drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

