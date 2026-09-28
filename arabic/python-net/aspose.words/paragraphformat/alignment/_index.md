---
title: ParagraphFormat.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "ParagraphFormat.alignment property. Gets or sets text alignment for the paragraph."
type: docs
weight: 30
url: /ar/python-net/aspose.words/paragraphformat/alignment/
---

## ParagraphFormat.alignment property

Gets or sets text alignment for the paragraph.


```python
@property
def alignment(self) -> aspose.words.ParagraphAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.ParagraphAlignment):
    ...

```

### Examples

Shows how to insert a paragraph into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Arial'
font.underline = aw.Underline.DASH
paragraph_format = builder.paragraph_format
paragraph_format.first_line_indent = 8
paragraph_format.alignment = aw.ParagraphAlignment.JUSTIFY
paragraph_format.add_space_between_far_east_and_alpha = True
paragraph_format.add_space_between_far_east_and_digit = True
paragraph_format.keep_together = True
# طريقة \"Writeln\" تنهي الفقرة بعد إلحاق النص
# ثم تبدأ سطرًا جديدًا، مضيفة فقرة جديدة.
builder.writeln('Hello world!')
self.assertTrue(builder.current_paragraph.is_end_of_document)
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
* class [ParagraphFormat](../)

