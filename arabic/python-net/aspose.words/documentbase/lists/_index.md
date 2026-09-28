---
title: DocumentBase.lists property
linktitle: lists property
articleTitle: lists property
second_title: Aspose.Words for Python
description: "DocumentBase.lists property. Provides access to the list formatting used in the document."
type: docs
weight: 50
url: /ar/python-net/aspose.words/documentbase/lists/
---

## DocumentBase.lists property

Provides access to the list formatting used in the document.


```python
@property
def lists(self) -> aspose.words.lists.ListCollection:
    ...

```

### Remarks

For more information see the description of the [ListCollection](../../../aspose.words.lists/listcollection/) class.




### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام مُنشئ المستند.
# 1 -  قائمة مرقمة:
# القوائم المرقمة تُنشئ ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# عن طريق ضبط خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
# لبدء قائمة فرعية مستقلة عند العنصر الحالي في القائمة.
# قالب قائمة Microsoft Word المسمى "NumberDefault" يستخدم الأرقام لإنشاء مستويات القائمة للمستوى الأول.
# المستويات الأعمق للقائمة تستخدم الأحرف والأرقام الرومانية الصغيرة.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  قائمة نقطية:
# هذه القائمة ستضيف مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
# المستويات الأعمق لهذه القائمة ستستخدم رموزًا مختلفة، مثل "■" و "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# يمكننا تعطيل تنسيق القوائم لتجنب تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين العلم "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [List](../../../aspose.words.lists/list/)
* class [ListFormat](../../../aspose.words.lists/listformat/)

