---
title: ParagraphAlignment enumeration
linktitle: ParagraphAlignment enumeration
articleTitle: ParagraphAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphAlignment enumeration. Specifies text alignment in a paragraph."
type: docs
weight: 970
url: /ar/python-net/aspose.words/paragraphalignment/
---

## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.


### Members

| Name | Description |
| --- | --- |
| LEFT | Text is aligned to the left. |
| CENTER | Text is centered horizontally. |
| RIGHT | Text is aligned to the right. |
| JUSTIFY | Text is aligned to both left and right. |
| DISTRIBUTED | Text is evenly distributed. |
| ARABIC_MEDIUM_KASHIDA | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ARABIC_HIGH_KASHIDA | Arabic only. Kashida length for text is extended to its widest possible length. |
| ARABIC_LOW_KASHIDA | Arabic only. Kashida length for text is extended to a slightly longer length. |
| THAI_DISTRIBUTED | Thai only. Text is justified with an optimization for Thai. |
| MATH_ELEMENT_CENTER_AS_GROUP | The only Math element in a line, aligned as 'Centered As Group'. |

### Examples

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

* module [aspose.words](../)

