---
title: Node.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "Node.get_text method. Gets the text of this node and of all its children."
type: docs
weight: 450
url: /ar/python-net/aspose.words/node/get_text/
---

## get_text() {#default}

Gets the text of this node and of all its children.


```python
def get_text(self):
    ...
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج فقرات بنص باستخدام DocumentBuilder.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# تحويل المستند إلى صيغة نصية يكشف أن الأحرف التحكمية
# تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# عند تحويل مستند إلى صيغة سلسلة،
# يمكننا حذف بعض الأحرف التحكمية باستخدام طريقة Trim.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# المستند الفارغ يحتوي على قسم واحد، جسم واحد وفقرة واحدة.
# استدعِ طريقة "RemoveAllChildren" لإزالة جميع تلك العقد،
# وانتهي بعقدة مستند بدون أي أطفال.
doc.remove_all_children()
# هذا المستند الآن لا يحتوي على أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
# إذا أردنا تحريره، سنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
# أولاً، أنشئ قسمًا جديدًا، ثم أضفه كطفل إلى عقدة المستند الجذرية.
section = aw.Section(doc)
doc.append_child(section)
# عيّن بعض خصائص إعداد الصفحة للقسم.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# القسم يحتاج إلى جسم، سيحتوي ويعرض جميع محتوياته
# على الصفحة بين رأس وتذييل القسم.
body = aw.Body(doc)
section.append_child(body)
# أنشئ فقرة، عيّن بعض خصائص التنسيق، ثم أضفها كطفل إلى الجسم.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# أخيرًا، أضف بعض المحتوى إلى المستند. أنشئ مقطعًا،
# عيّن مظهره ومحتوياته، ثم أضفه كطفل إلى الفقرة.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

