---
title: ListLevel.linked_style property
linktitle: linked_style property
articleTitle: linked_style property
second_title: Aspose.Words for Python
description: "ListLevel.linked_style property. Gets or sets the paragraph style that is linked to this list level."
type: docs
weight: 60
url: /ar/python-net/aspose.words.lists/listlevel/linked_style/
---

## ListLevel.linked_style property

Gets or sets the paragraph style that is linked to this list level.


```python
@property
def linked_style(self) -> aspose.words.Style:
    ...

@linked_style.setter
def linked_style(self, value: aspose.words.Style):
    ...

```

### Remarks

This property is ``None`` when the list level is not linked to a paragraph style.
This property can be set to ``None``.




### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# ستُنسق تسميات المستوى 1 وفق نمط الفقرة "Heading 1" وستحمل بادئة.
# ستظهر هكذا "Appendix A", "Appendix B"...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# ستعرض تسميات المستوى 2 الأرقام الحالية للمستوى الأول والثاني من القوائم وستحتوي على أصفار بادئة.
# إذا كان المستوى الأول للقائمة هو 1، فإن تسميات القائمة من هذه ستظهر كـ "Section (1.01)", "Section (1.02)"...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# لاحظ أن المستوى الأعلى يستخدم ترقيم UppercaseLetter.
# يمكننا ضبط الخاصية "IsLegal" لاستخدام أرقام عربية للمستويات العليا من القائمة.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# ستكون تسميات المستوى 3 أرقامًا رومانية كبيرة مع بادئة ولاحقة وستُعاد بدءها عند كل عنصر من المستوى 1 في القائمة.
# ستظهر تسميات القائمة هذه كـ "-I-", "-II-"...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# اجعل تسميات جميع مستويات القائمة غامقة.
for level in doc_list.list_levels:
    level.font.bold = True
# طبق تنسيق القائمة على الفقرة الحالية.
builder.list_format.list = doc_list
# أنشئ عناصر القائمة التي ستعرض جميع المستويات الثلاثة لقائمتنا.
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

