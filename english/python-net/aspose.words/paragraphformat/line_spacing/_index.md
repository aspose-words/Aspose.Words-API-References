---
title: ParagraphFormat.line_spacing property
linktitle: line_spacing property
articleTitle: line_spacing property
second_title: Aspose.Words for Python
description: "ParagraphFormat.line_spacing property. Gets or sets the line spacing (in points) for the paragraph."
type: docs
weight: 190
url: /python-net/aspose.words/paragraphformat/line_spacing/
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
builder = aw.DocumentBuilder(doc)

# Below are three line spacing rules that we can define using the
# paragraph's "line_spacing_rule" property to configure spacing between paragraphs.
# 1 -  Set a minimum amount of spacing.
# This will give vertical padding to lines of text of any size
# that is too small to maintain the minimum line-height.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20

builder.writeln("Minimum line spacing of 20.")
builder.writeln("Minimum line spacing of 20.")

# 2 -  Set exact spacing.
# Using font sizes that are too large for the spacing will truncate the text.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5

builder.writeln("Line spacing of exactly 5.")
builder.writeln("Line spacing of exactly 5.")

# 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
# This kind of spacing will scale to different font sizes.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18

builder.writeln("Line spacing of 1.5 default lines.")
builder.writeln("Line spacing of 1.5 default lines.")

doc.save(ARTIFACTS_DIR + "ParagraphFormat.line_spacing.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

