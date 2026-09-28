---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /ar/python-net/aspose.words.lists/listformat/list_level_number/
---

## ListFormat.list_level_number property

Gets or sets the list level number (0 to 8) for the paragraph.


```python
@property
def list_level_number(self) -> int:
    ...

@list_level_number.setter
def list_level_number(self, value: int):
    ...

```

### Remarks

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [ListFormat.list](../list/) property is set to reference a valid list.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام منشئ المستند.
# 1 -  قائمة نقطية:
# هذه القائمة ستضيف مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# إنهاء القائمة النقطية.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  قائمة مرقمة:
# القوائم المرقمة تُنشئ ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.list_format.apply_number_default()
# هذه الفقرة هي العنصر الأول. العنصر الأول في قائمة مرقمة سيحمل الرمز "1." كرمز عنصر القائمة.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# استدعِ الطريقة "ListIndent" لزيادة المستوى الحالي للقائمة،
# والتي ستبدأ قائمة مستقلة جديدة، مع إزاحة أعمق، عند العنصر الحالي للمستوى الأول من القائمة.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# هذه هي العناصر الثلاثة الأولى في المستوى الثاني من القائمة، والتي ستحافظ على عدّ
# مستقل عن عدّ المستوى الأول من القائمة. وفقًا لتنسيق القائمة الحالي،
# ستحمل الرموز "a.", "b.", و "c.".
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# استدعِ الطريقة "ListOutdent" للعودة إلى المستوى السابق من القائمة.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# سيتابع هذان الفقرتان عدّ المستوى الأول من القائمة.
# ستحمل هذه العناصر الرموز "2.", و "3."
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# إذا زدنا مستوى القائمة إلى مستوى أضفنا إليه عناصر مسبقًا،
# ستكون القائمة المتداخلة منفصلة عن السابقة، وسيبدأ ترقيمها من البداية.
# ستحتوي عناصر القائمة هذه على رموز "a.", "b.", "c.", "d.", و "e".
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# قم بإلغاء إزاحة مستوى القائمة مرة أخرى.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# إنهاء القائمة المرقمة.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

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

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)

