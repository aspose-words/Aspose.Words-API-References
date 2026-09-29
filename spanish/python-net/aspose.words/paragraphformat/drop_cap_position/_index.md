---
title: ParagraphFormat.drop_cap_position property
linktitle: drop_cap_position property
articleTitle: drop_cap_position property
second_title: Aspose.Words for Python
description: "ParagraphFormat.drop_cap_position property. Gets or sets the position for a drop cap text."
type: docs
weight: 100
url: /es/python-net/aspose.words/paragraphformat/drop_cap_position/
---

## ParagraphFormat.drop_cap_position property

Gets or sets the position for a drop cap text.


```python
@property
def drop_cap_position(self) -> aspose.words.DropCapPosition:
    ...

@drop_cap_position.setter
def drop_cap_position(self, value: aspose.words.DropCapPosition):
    ...

```

### Examples

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
# Crear una lista de esquema para los encabezados.
outline_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 1')
# Crear una lista numerada.
numbered_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Numbered list item 1.')
# Cada párrafo que forma parte de una lista tendrá esta bandera.
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)
# Crear una lista con viñetas.
bulleted_list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln('Bulleted list item 1.')
builder.writeln('Bulleted list item 2.')
builder.paragraph_format.clear_formatting()
# Volver a la lista numerada.
builder.list_format.list = numbered_list
builder.writeln('Numbered list item 2.')
builder.writeln('Numbered list item 3.')
# Volver a la lista de esquema.
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 2')
builder.paragraph_format.clear_formatting()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.NestedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

