---
title: LineSpacingRule enumeration
linktitle: LineSpacingRule enumeration
articleTitle: LineSpacingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineSpacingRule enumeration. Specifies line spacing values for a paragraph."
type: docs
weight: 730
url: /de/python-net/aspose.words/linespacingrule/
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
# Unten sind drei Zeilenabstandsregeln, die wir mithilfe der
# Paragraph‑Eigenschaft "LineSpacingRule" definieren können, um den Abstand zwischen Absätzen zu konfigurieren.
# 1 -  Setze einen minimalen Abstand fest.
# Dies gibt vertikalen Abstand zu Textzeilen jeder Größe
# die zu klein ist, um die minimale Zeilenhöhe beizubehalten.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  Setze genauen Abstand.
# Die Verwendung von Schriftgrößen, die zu groß für den Abstand sind, schneidet den Text ab.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  Setze den Abstand als Vielfaches des Standardzeilenabstands, der standardmäßig 12 Punkte beträgt.
# Diese Art von Abstand skaliert mit unterschiedlichen Schriftgrößen.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../)

