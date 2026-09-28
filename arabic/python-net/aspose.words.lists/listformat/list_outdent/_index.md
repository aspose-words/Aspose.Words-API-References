---
title: ListFormat.list_outdent method
linktitle: list_outdent method
articleTitle: list_outdent method
second_title: Aspose.Words for Python
description: "ListFormat.list_outdent method. Decreases the list level of the current paragraph by one level."
type: docs
weight: 80
url: /ar/python-net/aspose.words.lists/listformat/list_outdent/
---

## list_outdent() {#default}

Decreases the list level of the current paragraph by one level.


```python
def list_outdent(self):
    ...
```

### Remarks

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting
for each level specifies what bullet or number is used, left indent, space between
the bullet and text etc.




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

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

