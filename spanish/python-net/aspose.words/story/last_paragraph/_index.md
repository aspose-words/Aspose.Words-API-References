---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /es/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# El generador de documentos tiene un cursor, que actúa como la parte del documento
# donde el generador agrega nuevos nodos cuando usamos sus métodos de construcción de documentos.
# Este cursor funciona de la misma manera que el cursor intermitente de Microsoft Word,
# y también siempre termina inmediatamente después de cualquier nodo que el generador acaba de insertar.
# Para agregar contenido a una parte diferente del documento,
# podemos mover el cursor a un nodo diferente con el método "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# El cursor ahora está delante del nodo al que lo movimos.
# Agregar una segunda ejecución lo insertará delante de la primera ejecución.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Mueva el cursor al final del documento para continuar añadiendo texto al final como antes.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

