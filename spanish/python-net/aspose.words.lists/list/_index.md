---
title: List class
linktitle: List class
articleTitle: List class
second_title: Aspose.Words for Python
description: "aspose.words.lists.List class. Represents formatting of a list"
type: docs
weight: 10
url: /es/python-net/aspose.words.lists/list/
---

## List class

Represents formatting of a list.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

A list in a Microsoft Word document is a set of list formatting properties.
Each list can have up to 9 levels and formatting properties, such as number style, start value,
indent, tab position etc are defined separately for each level.

A [List](./) object always belongs to the [ListCollection](../listcollection/) collection.

To create a new list, use the Add methods of the [ListCollection](../listcollection/) collection.

To modify formatting of a list, use [ListLevel](../listlevel/) objects found in
the [List.list_levels](./list_levels/) collection.

To apply or remove list formatting from a paragraph, use [ListFormat](../listformat/).




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the owner document. |
| [is_list_style_definition](./is_list_style_definition/) | Returns ``True`` if this list is a definition of a list style. |
| [is_list_style_reference](./is_list_style_reference/) | Returns ``True`` if this list is a reference to a list style. |
| [is_multi_level](./is_multi_level/) | Returns ``True`` when the list contains 9 levels; ``False`` when 1 level. |
| [is_restart_at_each_section](./is_restart_at_each_section/) | Specifies whether list should be restarted at each section. Default value is ``False``. |
| [list_id](./list_id/) | Gets the unique identifier of the list. |
| [list_levels](./list_levels/) | Gets the collection of list levels for this list. |
| [style](./style/) | Gets the list style that this list references or defines. |

### Methods

| Name | Description |
| --- | --- |
|[ compare_to(obj)](./compare_to/#object) | Compares the specified object to the current object. |
|[ compare_to(other)](./compare_to/#list) | Compares the specified list to the current list. |
|[ equals(list)](./equals/#list) | Compares with the specified list. |
|[ has_same_template(other)](./has_same_template/#list) | Returns true if the current list and the given list are created from the same template. |

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

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
# Crea una lista a partir de una plantilla de Microsoft Word y personaliza los dos primeros niveles de su lista.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# Este valor NumberFormat creará símbolos de viñetas en forma de estrella.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Crea párrafos y aplica ambos niveles de lista de nuestro formato de lista personalizado a ellos.
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
# Crea una lista a partir de una plantilla de Microsoft Word y personaliza su primer nivel de lista.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Aplica nuestra lista a algunos párrafos.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# Podemos agregar una copia de una lista existente a la colección de listas del documento
# para crear una lista similar sin hacer cambios en la original.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Aplica la segunda lista a nuevos párrafos.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

### See Also

* module [aspose.words.lists](../)
* class [ListCollection](../listcollection/)
* class [ListLevel](../listlevel/)
* class [ListFormat](../listformat/)

