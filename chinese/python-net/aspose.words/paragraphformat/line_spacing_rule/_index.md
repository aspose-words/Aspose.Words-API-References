---
title: ParagraphFormat.line_spacing_rule property
linktitle: line_spacing_rule property
articleTitle: line_spacing_rule property
second_title: Aspose.Words for Python
description: "ParagraphFormat.line_spacing_rule property. Gets or sets the line spacing for the paragraph."
type: docs
weight: 200
url: /zh/python-net/aspose.words/paragraphformat/line_spacing_rule/
---

## ParagraphFormat.line_spacing_rule property

Gets or sets the line spacing for the paragraph.


```python
@property
def line_spacing_rule(self) -> aspose.words.LineSpacingRule:
    ...

@line_spacing_rule.setter
def line_spacing_rule(self, value: aspose.words.LineSpacingRule):
    ...

```

### Examples

Shows how to work with line spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 以下是我们可以使用的三条行间距规则，使用
# 段落的 "LineSpacingRule" 属性来配置段落之间的间距。
# 1 - 设置最小间距。
# 这将为任意大小的文本行提供垂直填充。
# 这对于保持最小行高来说太小。
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 - 设置精确间距。
# 使用对间距来说过大的字体大小会截断文本。
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 - 将间距设置为默认行间距的倍数，默认情况下为 12 点。
# 这种间距会根据不同的字体大小进行缩放。
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

