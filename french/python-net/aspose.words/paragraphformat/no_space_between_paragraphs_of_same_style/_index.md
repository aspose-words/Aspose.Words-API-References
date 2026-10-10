---
title: ParagraphFormat.no_space_between_paragraphs_of_same_style property
linktitle: no_space_between_paragraphs_of_same_style property
articleTitle: no_space_between_paragraphs_of_same_style property
second_title: Aspose.Words for Python
description: "ParagraphFormat.no_space_between_paragraphs_of_same_style property. When ``True``, [ParagraphFormat.space_before](../space_before/) and [ParagraphFormat.space_after](../space_after/) will be ignored between the paragraphs of the same style."
type: docs
weight: 250
url: /fr/python-net/aspose.words/paragraphformat/no_space_between_paragraphs_of_same_style/
---

## ParagraphFormat.no_space_between_paragraphs_of_same_style property

When ``True``, [ParagraphFormat.space_before](../space_before/) and [ParagraphFormat.space_after](../space_after/) will be ignored
between the paragraphs of the same style.



```python
@property
def no_space_between_paragraphs_of_same_style(self) -> bool:
    ...

@no_space_between_paragraphs_of_same_style.setter
def no_space_between_paragraphs_of_same_style(self, value: bool):
    ...

```

### Remarks

This setting only takes affect when applied to a paragraph style. If applied to
a paragraph directly, it has no effect.




### Examples

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Appliquez une grande quantité d'espacement avant et après les paragraphes que ce constructeur créera.
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# Définissez le drapeau "NoSpaceBetweenParagraphsOfSameStyle" sur "true" pour appliquer
# aucun espacement entre les paragraphes du même style, ce qui regroupera les paragraphes similaires.
# Laissez le drapeau "NoSpaceBetweenParagraphsOfSameStyle" sur "false"
# pour appliquer uniformément l'espacement à chaque paragraphe.
builder.paragraph_format.no_space_between_paragraphs_of_same_style = no_space_between_paragraphs_of_same_style
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Quote')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingSameStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

