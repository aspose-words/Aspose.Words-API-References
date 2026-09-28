---
title: ListFormat.is_list_item property
linktitle: is_list_item property
articleTitle: is_list_item property
second_title: Aspose.Words for Python
description: "ListFormat.is_list_item property. True when the paragraph has bulleted or numbered formatting applied to it."
type: docs
weight: 10
url: /ar/python-net/aspose.words.lists/listformat/is_list_item/
---

## ListFormat.is_list_item property

True when the paragraph has bulleted or numbered formatting applied to it.


```python
@property
def is_list_item(self) -> bool:
    ...

```

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

Shows how to output all paragraphs in a document that are list items.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
builder.list_format.apply_bullet_default()
builder.writeln('Bulleted list item 1')
builder.writeln('Bulleted list item 2')
builder.writeln('Bulleted list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
for para in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'This paragraph belongs to list ID# {para.list_format.list.list_id}, number style "{para.list_format.list_level.number_style}"')
    print(f'\t"{para.get_text().strip()}"')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

