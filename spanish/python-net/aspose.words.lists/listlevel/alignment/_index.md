---
title: ListLevel.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "ListLevel.alignment property. Gets or sets the justification of the actual number of the list item."
type: docs
weight: 10
url: /es/python-net/aspose.words.lists/listlevel/alignment/
---

## ListLevel.alignment property

Gets or sets the justification of the actual number of the list item.


```python
@property
def alignment(self) -> aspose.words.lists.ListLevelAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.lists.ListLevelAlignment):
    ...

```

### Remarks

The list label is justified relative to the [ListLevel.number_position](../number_position/) property.




### Examples

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

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

