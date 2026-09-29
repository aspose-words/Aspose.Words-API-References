---
title: LineSpacingRule enumeration
linktitle: LineSpacingRule enumeration
articleTitle: LineSpacingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineSpacingRule enumeration. Specifies line spacing values for a paragraph."
type: docs
weight: 730
url: /it/python-net/aspose.words/linespacingrule/
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
# Di seguito sono riportate tre regole di interlinea che possiamo definire usando il
# proprietà "LineSpacingRule" del paragrafo per configurare la spaziatura tra i paragrafi.
# 1 -  Imposta una quantità minima di spaziatura.
# Questo fornirà un'imbottitura verticale alle righe di testo di qualsiasi dimensione
# che è troppo piccola per mantenere l'altezza minima della riga.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  Imposta una spaziatura esatta.
# Usare dimensioni di carattere troppo grandi per la spaziatura troncherà il testo.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  Imposta la spaziatura come un multiplo della spaziatura di linea predefinita, che è di 12 punti per impostazione predefinita.
# Questo tipo di spaziatura si adatterà a diverse dimensioni di carattere.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../)

