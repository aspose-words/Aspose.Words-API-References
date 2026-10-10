---
title: Paragraph.is_list_item property
linktitle: is_list_item property
articleTitle: is_list_item property
second_title: Aspose.Words for Python
description: "Paragraph.is_list_item property. True when the paragraph is an item in a bulleted or numbered list in original revision."
type: docs
weight: 120
url: /ar/python-net/aspose.words/paragraph/is_list_item/
---

## Paragraph.is_list_item property

True when the paragraph is an item in a bulleted or numbered list in original revision.


```python
@property
def is_list_item(self) -> bool:
    ...

```

### Examples

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# إنشاء قائمة مخطط للعناوين.
outline_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 1')
# إنشاء قائمة مرقمة.
numbered_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Numbered list item 1.')
# كل فقرة تشكل قائمة ستحمل هذه العلامة.
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)
# إنشاء قائمة نقطية.
bulleted_list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln('Bulleted list item 1.')
builder.writeln('Bulleted list item 2.')
builder.paragraph_format.clear_formatting()
# العودة إلى القائمة المرقمة.
builder.list_format.list = numbered_list
builder.writeln('Numbered list item 2.')
builder.writeln('Numbered list item 3.')
# العودة إلى قائمة المخطط.
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 2')
builder.paragraph_format.clear_formatting()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.NestedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

