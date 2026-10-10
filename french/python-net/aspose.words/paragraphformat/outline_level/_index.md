---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /fr/python-net/aspose.words/paragraphformat/outline_level/
---

## ParagraphFormat.outline_level property

Specifies the outline level of the paragraph in the document.


```python
@property
def outline_level(self) -> aspose.words.OutlineLevel:
    ...

@outline_level.setter
def outline_level(self, value: aspose.words.OutlineLevel):
    ...

```

### Examples

Shows how to configure paragraph outline levels to create collapsible text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Chaque paragraphe possède un OutlineLevel, qui peut être n'importe quel nombre de 1 à 9, ou la valeur par défaut "BodyText".
# Définir la propriété sur l'une des valeurs numérotées affichera une flèche à gauche
# du début du paragraphe.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# Le niveau 1 est le niveau le plus élevé. S'il existe un paragraphe de niveau inférieur sous un paragraphe de niveau supérieur,
# réduire le paragraphe de niveau supérieur réduira le paragraphe de niveau inférieur.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# Deux paragraphes du même niveau ne se réduiront pas l'un l'autre,
# et les flèches ne réduisent pas les paragraphes vers lesquels elles pointent.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# La valeur par défaut "BodyText" est la plus basse, qu'un paragraphe de n'importe quel niveau peut réduire.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

