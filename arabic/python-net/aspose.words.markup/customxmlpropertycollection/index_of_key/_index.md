---
title: CustomXmlPropertyCollection.index_of_key method
linktitle: index_of_key method
articleTitle: index_of_key method
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.index_of_key method. Returns the zero-based index of the specified property in the collection."
type: docs
weight: 70
url: /ar/python-net/aspose.words.markup/customxmlpropertycollection/index_of_key/
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
# تظهر علامة ذكية في مستند مع Microsoft Word عندما يتعرف على جزء من نصه كنوع من البيانات،
# مثل اسم أو تاريخ أو عنوان، ويحولها إلى ارتباط تشعبي يعرض خطًا سفليًا منقّطًا أرجوانيًا.
# في Word 2003، يمكننا تمكين العلامات الذكية عبر "Tools" -> "AutoCorrect options..." -> "SmartTags".
# في مستند الإدخال الخاص بنا، هناك ثلاثة كائنات سجّلتها Microsoft Word كعلامات ذكية.
# قد تكون العلامات الذكية متداخلة، لذا تحتوي هذه المجموعة على المزيد.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# يحتوي العضو "Properties" في العلامة الذكية على بياناته التعريفية، والتي ستختلف لكل نوع من العلامات الذكية.
# تحتوي خصائص العلامة الذكية من نوع "date" على السنة والشهر واليوم.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# يمكننا أيضًا الوصول إلى الخصائص بطرق مختلفة، مثل زوج المفتاح-القيمة.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# أدناه ثلاث طرق لإزالة العناصر من مجموعة الخصائص.
# 1 -  إزالة حسب الفهرس:
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  إزالة حسب الاسم:
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  مسح المجموعة بالكامل مرة واحدة:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)

