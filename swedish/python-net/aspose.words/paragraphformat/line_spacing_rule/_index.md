---
title: ParagraphFormat.line_spacing_rule property
linktitle: line_spacing_rule property
articleTitle: line_spacing_rule property
second_title: Aspose.Words for Python
description: "ParagraphFormat.line_spacing_rule property. Gets or sets the line spacing for the paragraph."
type: docs
weight: 200
url: /sv/python-net/aspose.words/paragraphformat/line_spacing_rule/
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
# Nedan är tre radavståndsregler som vi kan definiera med hjälp av
# styckets \"LineSpacingRule\"‑egenskap för att konfigurera avståndet mellan stycken.
# 1 -  Ställ in ett minsta avstånd.
# Detta ger vertikal utfyllnad till textrader av vilken storlek som helst
# som är för liten för att upprätthålla minsta radavstånd.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  Ställ in exakt avstånd.
# Att använda teckenstorlekar som är för stora för avståndet kommer att trunkera texten.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  Ställ in avstånd som en multipel av standardradavstånd, vilket som standard är 12 punkter.
# Denna typ av avstånd kommer att skalas till olika teckenstorlekar.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

