---
title: ParagraphFormat.is_heading property
linktitle: is_heading property
articleTitle: is_heading property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_heading property. True when the paragraph style is one of the built-in Heading styles."
type: docs
weight: 140
url: /ar/python-net/aspose.words/paragraphformat/is_heading/
---

## ParagraphFormat.is_heading property

True when the paragraph style is one of the built-in Heading styles.


```python
@property
def is_heading(self) -> bool:
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج عناوين يمكن أن تكون مدخلات جدول المحتويات للمستويات 1، 2، ثم 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
save_options = aw.saving.PdfSaveOptions()
save_options.save_format = aw.SaveFormat.PDF
# سيحتوي مستند PDF الناتج على مخطط، وهو جدول محتويات يسرد العناوين في جسم المستند.
# النقر على مدخل في هذا المخطط سيأخذنا إلى موقع العنوان المقابل له.
# تعيين خاصية "HeadingsOutlineLevels" إلى "2" لاستبعاد جميع العناوين التي مستوياتها أعلى من 2 من المخطط.
# العناوين الأخيرة الاثنين التي أدخلناها أعلاه لن تظهر.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HeadingsOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

