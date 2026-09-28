---
title: XpsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/xpssaveoptions/save_format/
---

## XpsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

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
# أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .XPS.
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# سيتضمن مستند XPS الناتج مخططًا، جدول محتويات يسرد العناوين في جسم المستند.
# النقر على مدخل في هذا المخطط سيأخذنا إلى موقع العنوان المقابل له.
# تعيين خاصية "HeadingsOutlineLevels" إلى "2" لاستبعاد جميع العناوين التي مستوياتها أعلى من 2 من المخطط.
# العناوين الأخيرة الاثنين التي أدخلناها أعلاه لن تظهر.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

