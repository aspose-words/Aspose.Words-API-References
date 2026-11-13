---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /es/python-net/aspose.words/paragraphformat/lines_to_drop/
---

## ParagraphFormat.lines_to_drop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```python
@property
def lines_to_drop(self) -> int:
    ...

@lines_to_drop.setter
def lines_to_drop(self, value: int):
    ...

```

### Examples

Shows how to set the size of a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modifique la propiedad "LinesToDrop" para designar un párrafo como letra capitular,
# lo que lo convertirá en una letra mayúscula grande que decorará el siguiente párrafo.
# Asigne a esta propiedad el valor 4 para dar a la letra capitular una altura de cuatro líneas de texto.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# Restablezca la propiedad "LinesToDrop" a 0 para convertir el siguiente párrafo en un párrafo ordinario.
# El texto en este párrafo se envolverá alrededor de la letra capitular.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

