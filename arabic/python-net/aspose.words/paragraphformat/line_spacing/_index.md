---
title: ParagraphFormat.line_spacing property
linktitle: line_spacing property
articleTitle: line_spacing property
second_title: Aspose.Words for Python
description: "ParagraphFormat.line_spacing property. Gets or sets the line spacing (in points) for the paragraph."
type: docs
weight: 190
url: /ar/python-net/aspose.words/paragraphformat/line_spacing/
---

## ParagraphFormat.line_spacing property

Gets or sets the line spacing (in points) for the paragraph.


```python
@property
def line_spacing(self) -> float:
    ...

@line_spacing.setter
def line_spacing(self, value: float):
    ...

```

### Remarks

When [ParagraphFormat.line_spacing_rule](../line_spacing_rule/) property is set to [LineSpacingRule.AT_LEAST](../../linespacingrule/#AT_LEAST), the line spacing can be greater than or equal to,
but never less than the specified [ParagraphFormat.line_spacing](./) value.

When [ParagraphFormat.line_spacing_rule](../line_spacing_rule/) property is set to [LineSpacingRule.EXACTLY](../../linespacingrule/#EXACTLY), the line spacing never changes from
the specified [ParagraphFormat.line_spacing](./) value, even if a larger font is used within the paragraph.




### Examples

Shows how to work with line spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# فيما يلي ثلاث قواعد لتباعد الأسطر يمكننا تعريفها باستخدام
# خاصية "LineSpacingRule" للفقرة لتكوين التباعد بين الفقرات.
# 1 -  تعيين حد أدنى للتباعد.
# سيعطي هذا حشوة رأسية لسطور النص بأي حجم
# التي تكون صغيرة جدًا للحفاظ على الحد الأدنى لارتفاع السطر.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  تعيين تباعد دقيق.
# استخدام أحجام خطوط كبيرة جدًا بالنسبة للتباعد سيؤدي إلى قطع النص.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  تعيين التباعد كعدد مضاعف للتباعد الافتراضي للخط، والذي يكون 12 نقطة بشكل افتراضي.
# هذا النوع من التباعد سيتكيف مع أحجام خطوط مختلفة.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

