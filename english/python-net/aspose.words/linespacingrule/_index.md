---
title: LineSpacingRule enumeration
linktitle: LineSpacingRule enumeration
articleTitle: LineSpacingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineSpacingRule enumeration. Specifies line spacing values for a paragraph."
type: docs
weight: 720
url: /python-net/aspose.words/linespacingrule/
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
# Below are three line spacing rules that we can define using the
# paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
# 1 -  Set a minimum amount of spacing.
# This will give vertical padding to lines of text of any size
# that is too small to maintain the minimum line-height.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  Set exact spacing.
# Using font sizes that are too large for the spacing will truncate the text.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
# This kind of spacing will scale to different font sizes.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../)

