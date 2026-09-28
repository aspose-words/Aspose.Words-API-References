---
title: ListLevelCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ListLevelCollection.count property. Gets the number of levels in this list."
type: docs
weight: 20
url: /ar/python-net/aspose.words.lists/listlevelcollection/count/
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
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# يمكننا احتواء كائن List كامل داخل نمط.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# غيّر مظهر جميع مستويات القائمة في قائمتنا.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# أنشئ قائمة أخرى من قائمة داخل نمط.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# أضف بعض عناصر القائمة التي ستقوم قائمتنا بتنسيقها.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# أنشئ وطبق قائمة أخرى بناءً على نمط القائمة.
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

