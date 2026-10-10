---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /ar/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# يمتلك مُنشئ المستند مؤشرًا، يعمل كجزء من المستند
# حيث يضيف المُنشئ عقدًا جديدة عندما نستخدم طرق بناء المستند الخاصة به.
# يعمل هذا المؤشر بنفس طريقة مؤشر وميض Microsoft Word،
# كما أنه دائمًا ما ينتهي مباشرةً بعد أي عقدة أضافها المُنشئ للتو.
# لإضافة محتوى إلى جزء مختلف من المستند،
# يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# المؤشر الآن أمام العقدة التي نقلناه إليها.
# إضافة سلسلة ثانية ستُدرجها أمام السلسلة الأولى.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# حرك المؤشر إلى نهاية المستند لمتابعة إلحاق النص بالنهاية كما كان من قبل.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

