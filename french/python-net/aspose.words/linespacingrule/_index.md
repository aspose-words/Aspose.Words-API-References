---
title: LineSpacingRule enumeration
linktitle: LineSpacingRule enumeration
articleTitle: LineSpacingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineSpacingRule enumeration. Specifies line spacing values for a paragraph."
type: docs
weight: 730
url: /fr/python-net/aspose.words/linespacingrule/
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
# Voici trois règles d'interligne que nous pouvons définir en utilisant le
# propriété "LineSpacingRule" du paragraphe pour configurer l'espacement entre les paragraphes.
# 1 -  Définir une quantité minimale d'espacement.
# Cela ajoutera un remplissage vertical aux lignes de texte de toute taille
# qui est trop petite pour maintenir la hauteur de ligne minimale.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.AT_LEAST
builder.paragraph_format.line_spacing = 20
builder.writeln('Minimum line spacing of 20.')
builder.writeln('Minimum line spacing of 20.')
# 2 -  Définir un espacement exact.
# Utiliser des tailles de police trop grandes pour l'espacement tronquera le texte.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.EXACTLY
builder.paragraph_format.line_spacing = 5
builder.writeln('Line spacing of exactly 5.')
builder.writeln('Line spacing of exactly 5.')
# 3 -  Définir l'espacement comme un multiple de l'espacement de ligne par défaut, qui est de 12 points par défaut.
# Ce type d'espacement s'adaptera à différentes tailles de police.
builder.paragraph_format.line_spacing_rule = aw.LineSpacingRule.MULTIPLE
builder.paragraph_format.line_spacing = 18
builder.writeln('Line spacing of 1.5 default lines.')
builder.writeln('Line spacing of 1.5 default lines.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LineSpacing.docx')
```

### See Also

* module [aspose.words](../)

