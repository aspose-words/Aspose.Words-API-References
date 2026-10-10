---
title: OutlineLevel enumeration
linktitle: OutlineLevel enumeration
articleTitle: OutlineLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.OutlineLevel enumeration. Specifies the outline level of a paragraph in the document."
type: docs
weight: 890
url: /it/python-net/aspose.words/outlinelevel/
---

## OutlineLevel enumeration

Specifies the outline level of a paragraph in the document.


### Members

| Name | Description |
| --- | --- |
| LEVEL1 | The paragraph is at the outline level 1 (topmost level). |
| LEVEL2 | The paragraph is at the outline level 2. |
| LEVEL3 | The paragraph is at the outline level 3. |
| LEVEL4 | The paragraph is at the outline level 4. |
| LEVEL5 | The paragraph is at the outline level 5. |
| LEVEL6 | The paragraph is at the outline level 6. |
| LEVEL7 | The paragraph is at the outline level 7. |
| LEVEL8 | The paragraph is at the outline level 8. |
| LEVEL9 | The paragraph is at the outline level 9. |
| BODY_TEXT | The paragraph is at the level of the main text. |

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

* module [aspose.words](../)

