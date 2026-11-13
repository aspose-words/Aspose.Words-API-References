---
title: ListFormat.list property
linktitle: list property
articleTitle: list property
second_title: Aspose.Words for Python
description: "ListFormat.list property. Gets or sets the list this paragraph is a member of."
type: docs
weight: 20
url: /es/python-net/aspose.words.lists/listformat/list/
---

## ListFormat.list property

Gets or sets the list this paragraph is a member of.


```python
@property
def list(self) -> aspose.words.lists.List:
    ...

@list.setter
def list(self, value: aspose.words.lists.List):
    ...

```

### Remarks

The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to ``None`` removes bullets and numbering from the paragraph
and sets the list level number to zero. Setting this property to ``None`` is equivalent
to calling [ListFormat.remove_numbers()](../remove_numbers/#default).




### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
# A continuación se presentan dos tipos de listas que podemos crear usando un document builder.
# 1 -  Una lista numerada:
# Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
# para iniciar una sublista independiente en el elemento de lista actual.
# La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
# Los niveles de lista más profundos usan letras y números romanos en minúscula.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Una lista con viñetas:
# Esta lista aplicará una indentación y un símbolo de viñeta ("•") antes de cada párrafo.
# Los niveles más profundos de esta lista usarán símbolos diferentes, como "■" y "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Podemos desactivar el formato de lista para que los párrafos posteriores no se formateen como listas desactivando la bandera "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

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

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list_level_number](../list_level_number/)
* method [ListFormat.remove_numbers()](../remove_numbers/#default)

