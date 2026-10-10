---
title: ListLevelCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ListLevelCollection.count property. Gets the number of levels in this list."
type: docs
weight: 20
url: /zh/python-net/aspose.words.lists/listlevelcollection/count/
---

## ListLevelCollection.count property

Gets the number of levels in this list.


```python
@property
def count(self) -> int:
    ...

```

### Remarks

There could be 1 or 9 levels in a list.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
# 我们可以在样式中包含整个 List 对象。
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# 更改我们列表中所有列表层级的外观。
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# 从样式中的列表创建另一个列表。
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# 添加一些列表项，我们的列表将对其进行格式化。
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# 基于列表样式创建并应用另一个列表。
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevelCollection](../)

