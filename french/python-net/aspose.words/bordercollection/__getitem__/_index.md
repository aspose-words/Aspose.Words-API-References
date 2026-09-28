---
title: BorderCollection indexer
linktitle: BorderCollection indexer
articleTitle: BorderCollection indexer
second_title: Aspose.Words for Python
description: "BorderCollection indexer. Retrieves a [Border](../../border/) object by index."
type: docs
weight: 10
url: /fr/python-net/aspose.words/bordercollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Border](../../border/) object by index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how border collections can share elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1.')
builder.write('Paragraph 2.')
# Puisque nous avons utilisé la même configuration de bordure lors de la création
# de ces paragraphes, leurs collections de bordures partagent les mêmes éléments.
first_paragraph_borders = doc.first_section.body.first_paragraph.paragraph_format.borders
second_paragraph_borders = builder.current_paragraph.paragraph_format.borders
i = 0
while i < first_paragraph_borders.count:
    self.assertTrue(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    self.assertFalse(first_paragraph_borders[i].is_visible)
    i += 1
for border in second_paragraph_borders:
    border.line_style = aw.LineStyle.DOT_DASH
# Après avoir modifié le style de ligne des bordures uniquement dans le deuxième paragraphe,
# les collections de bordures ne partagent plus les mêmes éléments.
i = 0
while i < first_paragraph_borders.count:
    self.assertFalse(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertNotEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    # Modifier l'apparence d'une bordure vide la rend visible.
    self.assertTrue(second_paragraph_borders[i].is_visible)
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Border.SharedElements.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

