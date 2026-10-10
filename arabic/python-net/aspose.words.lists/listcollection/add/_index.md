---
title: ListCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListCollection.add method"
type: docs
weight: 40
url: /ar/python-net/aspose.words.lists/listcollection/add/
---

## add(list_template) {#listtemplate}

Creates a new list based on a predefined template and adds it to the collection of lists in the document.


```python
def add(self, list_template: aspose.words.lists.ListTemplate):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_template | [ListTemplate](../../listtemplate/) | The template of the list. |

### Remarks

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.

All lists created using this method have 9 list levels.




### Returns

The newly created list.


## add(list_style) {#style}

Creates a new list that references a list style and adds it to the collection of lists in the document.


```python
def add(self, list_style: aspose.words.Style):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_style | [Style](../../../aspose.words/style/) | The list style. |

### Remarks

The newly created list references the list style. If you change the properties of the list
style, it is reflected in the properties of the list. Vice versa, if you change the properties
of the list, it is reflected in the properties of the list style.




### Returns

The newly created list.


## Examples

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

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# إنشاء قائمة من قالب Microsoft Word، وتخصيص المستوى الأول من القائمة.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# تطبيق قائمتنا على بعض الفقرات.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قوائم المستند
# لإنشاء قائمة مشابهة دون تعديل الأصل.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# تطبيق القائمة الثانية على فقرات جديدة.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

Shows how to create a list by applying a new list format to a collection of paragraphs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1')
builder.writeln('Paragraph 2')
builder.write('Paragraph 3')
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_UPPERCASE_LETTER_DOT)
for paragraph in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras))):
    paragraph.list_format.list = doc_list
    paragraph.list_format.list_level_number = 1
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

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

## See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

