---
title: PdfSaveOptions.outline_options property
linktitle: outline_options property
articleTitle: outline_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.outline_options property. Allows to specify outline options."
type: docs
weight: 260
url: /ar/python-net/aspose.words.saving/pdfsaveoptions/outline_options/
---

## PdfSaveOptions.outline_options property

Allows to specify outline options.


```python
@property
def outline_options(self) -> aspose.words.saving.OutlineOptions:
    ...

```

### Remarks

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [PdfSaveOptions.outline_options](./) class.




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

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إدراج عناوين يمكن أن تكون مدخلات جدول المحتويات للمستويات 1 و 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
save_options = aw.saving.PdfSaveOptions()
# سيحتوي مستند PDF الناتج على مخطط، وهو جدول محتويات يسرد العناوين في جسم المستند.
# النقر على مدخل في هذا المخطط سيأخذنا إلى موقع العنوان المقابل له.
# ضبط الخاصية "HeadingsOutlineLevels" إلى "5" لتضمين جميع العناوين من المستوى 5 وما أدناه في المخطط.
save_options.outline_options.headings_outline_levels = 5
# يحتوي هذا المستند على عناوين بالمستوى 1 و 5، ولا توجد عناوين بالمستوى 2 و 3 و 4.
# سيعامل مستند PDF الناتج مستويات المخطط 2 و 3 و 4 كـ "مفقودة".
# ضبط الخاصية "CreateMissingOutlineLevels" إلى "true" لتضمين جميع المستويات المفقودة في المخطط،
# مما يترك مدخلات مخطط فارغة لأنه لا توجد عناوين صالحة للاستخدام.
# ضبط الخاصية "CreateMissingOutlineLevels" إلى "false" لتجاهل المستويات المفقودة في المخطط،
# وتعامل عناوين المستوى 5 في المخطط كمستوى 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

