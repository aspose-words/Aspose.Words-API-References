---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /ar/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

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
* class [OutlineOptions](../)

