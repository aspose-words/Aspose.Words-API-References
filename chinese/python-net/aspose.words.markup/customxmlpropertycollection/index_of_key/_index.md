---
title: CustomXmlPropertyCollection.index_of_key method
linktitle: index_of_key method
articleTitle: index_of_key method
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.index_of_key method. Returns the zero-based index of the specified property in the collection."
type: docs
weight: 70
url: /zh/python-net/aspose.words.markup/customxmlpropertycollection/index_of_key/
---

## index_of_key(name) {#str}

Returns the zero-based index of the specified property in the collection.


```python
def index_of_key(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The case-sensitive name of the property. |

### Returns

The zero based index. Negative value if not found.


### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# 当 Microsoft Word 在文档中识别出其文本的一部分为某种数据时，会出现智能标签，
# 例如姓名、日期或地址，并将其转换为显示紫色点状下划线的超链接。
# 在 Word 2003 中，我们可以通过 "Tools" -> "AutoCorrect options..." -> "SmartTags" 来启用智能标签。
# 在我们的输入文档中，有三个对象被 Microsoft Word 注册为智能标签。
# 智能标签可能是嵌套的，因此此集合包含更多。
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# 智能标签的 "Properties" 成员包含其元数据，不同类型的智能标签会有所不同。
# "date" 类型智能标签的属性包含其年份、月份和日期。
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# 我们还可以通过多种方式访问这些属性，例如键值对。
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# 下面是从属性集合中移除元素的三种方法。
# 1 -  按索引删除：
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  按名称删除：
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 - 一次性清除整个集合：
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)

