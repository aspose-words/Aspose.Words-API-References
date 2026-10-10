---
title: Section.page_setup property
linktitle: page_setup property
articleTitle: page_setup property
second_title: Aspose.Words for Python
description: "Section.page_setup property. Returns an object that represents page setup and section properties."
type: docs
weight: 50
url: /ar/python-net/aspose.words/section/page_setup/
---

## Section.page_setup property

Returns an object that represents page setup and section properties.


```python
@property
def page_setup(self) -> aspose.words.PageSetup:
    ...

```

### Examples

Shows how to create a wide blue band border at the top of the first page.

```python
doc = aw.Document()
page_setup = doc.sections[0].page_setup
page_setup.border_always_in_front = False
page_setup.border_distance_from = aw.PageBorderDistanceFrom.PAGE_EDGE
page_setup.border_applies_to = aw.PageBorderAppliesTo.FIRST_PAGE
border = page_setup.borders.get_by_border_type(aw.BorderType.TOP)
border.line_style = aw.LineStyle.SINGLE
border.line_width = 30
border.color = aspose.pydrawing.Color.blue
border.distance_from_text = 0
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorderProperties.docx')
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
* class [Section](../)

