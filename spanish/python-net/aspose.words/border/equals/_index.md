---
title: Border.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "Border.equals method. Determines whether the specified border is equal in value to the current border."
type: docs
weight: 100
url: /es/python-net/aspose.words/border/equals/
---

## equals(rhs) {#border}

Determines whether the specified border is equal in value to the current border.


```python
def equals(self, rhs: aspose.words.Border):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Border](../) |  |

### Examples

Shows how border collections can share elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1.')
builder.write('Paragraph 2.')
# Dado que usamos la misma configuración de bordes al crear
# estos párrafos, sus colecciones de bordes comparten los mismos elementos.
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
# Después de cambiar el estilo de línea de los bordes solo en el segundo párrafo,
# las colecciones de bordes ya no comparten los mismos elementos.
i = 0
while i < first_paragraph_borders.count:
    self.assertFalse(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertNotEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    # Cambiar la apariencia de un borde vacío lo hace visible.
    self.assertTrue(second_paragraph_borders[i].is_visible)
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Border.SharedElements.docx')
```

### See Also

* module [aspose.words](../../)
* class [Border](../)

