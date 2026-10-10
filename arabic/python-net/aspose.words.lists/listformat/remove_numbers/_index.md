---
title: ListFormat.remove_numbers method
linktitle: remove_numbers method
articleTitle: remove_numbers method
second_title: Aspose.Words for Python
description: "ListFormat.remove_numbers method. Removes numbers or bullets from the current paragraph and sets list level to zero."
type: docs
weight: 90
url: /ar/python-net/aspose.words.lists/listformat/remove_numbers/
---

## remove_numbers() {#default}

Removes numbers or bullets from the current paragraph and sets list level to zero.


```python
def remove_numbers(self):
    ...
```

### Remarks

Calling this method is equivalent to setting the [ListFormat.list](../list/) property to ``None``.




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

Shows how to remove list formatting from all paragraphs in the main text of a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
for paragraph in paras:
    paragraph = paragraph.as_paragraph()
    paragraph.list_format.remove_numbers()
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

