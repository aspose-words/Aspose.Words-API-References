---
title: OutlineOptions.expanded_outline_levels property
linktitle: expanded_outline_levels property
articleTitle: expanded_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.expanded_outline_levels property. Specifies how many levels in the document outline to show expanded when the file is viewed."
type: docs
weight: 60
url: /ar/python-net/aspose.words.saving/outlineoptions/expanded_outline_levels/
---

## OutlineOptions.expanded_outline_levels property

Specifies how many levels in the document outline to show expanded when the file is viewed.


```python
@property
def expanded_outline_levels(self) -> int:
    ...

@expanded_outline_levels.setter
def expanded_outline_levels(self, value: int):
    ...

```

### Remarks

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items
in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج عناوين بالمستويات من 1 إلى 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# سيحتوي مستند PDF الناتج على مخطط، وهو جدول محتويات يسرد العناوين في جسم المستند.
# النقر على مدخل في هذا المخطط سيأخذنا إلى موقع العنوان المقابل له.
# اضبط خاصية "HeadingsOutlineLevels" إلى "4" لاستبعاد جميع العناوين التي مستوياتها فوق 4 من المخطط.
options.outline_options.headings_outline_levels = 4
# إذا كان لمدخل المخطط مدخلات لاحقة ذات مستوى أعلى بينه وبين المدخل التالي من نفس المستوى أو مستوى أدنى،
# ستظهر سهم إلى يسار المدخل. هذا المدخل هو "المالك" لعدة "مدخلات فرعية" مماثلة.
# في مستندنا، مدخلات المخطط من المستوى الخامس هي مدخلات فرعية للمدخل الثاني من المستوى الرابع في المخطط،
# الإدخالات من المستوى الرابع والخامس هي إدخالات فرعية للإدخال الثاني من المستوى الثالث، وهكذا.
# في المخطط، يمكننا النقر على السهم الخاص بإدخال "owner" لتقليص/توسيع جميع الإدخالات الفرعية الخاصة به.
# قم بتعيين الخاصية "ExpandedOutlineLevels" إلى "2" لتوسيع جميع إدخالات المخطط من المستوى 2 وما أدناه تلقائيًا
# وتقليص جميع الإدخالات من المستوى 3 وما أعلى عند فتح المستند.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

