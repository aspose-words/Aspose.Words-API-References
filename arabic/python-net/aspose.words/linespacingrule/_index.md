---
title: LineSpacingRule enumeration
linktitle: LineSpacingRule enumeration
articleTitle: LineSpacingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineSpacingRule enumeration. Specifies line spacing values for a paragraph."
type: docs
weight: 730
url: /ar/python-net/aspose.words/linespacingrule/
---

## LineSpacingRule enumeration

Specifies line spacing values for a paragraph.


### Members

| Name | Description |
| --- | --- |
| AT_LEAST | The line spacing can be greater than or equal to, but never less than, the value specified in the [ParagraphFormat.line_spacing](../paragraphformat/line_spacing/) property. |
| EXACTLY | The line spacing never changes from the value specified in the [ParagraphFormat.line_spacing](../paragraphformat/line_spacing/) property, even if a larger font is used within the paragraph. |
| MULTIPLE | The line spacing is specified in the [ParagraphFormat.line_spacing](../paragraphformat/line_spacing/) property as the number of lines. One line equals 12 points. |

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

* module [aspose.words](../)

