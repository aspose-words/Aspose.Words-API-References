---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /it/python-net/aspose.words/paragraphformat/outline_level/
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
# Ogni paragrafo ha un OutlineLevel, che può essere qualsiasi numero da 1 a 9, o al valore predefinito "BodyText".
# Impostare la proprietà su uno dei valori numerati mostrerà una freccia a sinistra
# all'inizio del paragrafo.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# Il livello 1 è il livello più alto. Se c'è un paragrafo con un livello inferiore sotto un paragrafo con un livello superiore,
# comprimere il paragrafo di livello superiore comprimerà il paragrafo di livello inferiore.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# Due paragrafi dello stesso livello non si comprimeranno a vicenda,
# e le frecce non comprimono i paragrafi a cui puntano.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# Il valore predefinito "BodyText" è il più basso, che un paragrafo di qualsiasi livello può comprimere.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

