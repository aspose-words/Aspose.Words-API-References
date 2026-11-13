---
title: List.is_list_style_definition property
linktitle: is_list_style_definition property
articleTitle: is_list_style_definition property
second_title: Aspose.Words for Python
description: "List.is_list_style_definition property. Returns ``True`` if this list is a definition of a list style."
type: docs
weight: 20
url: /es/python-net/aspose.words.lists/list/is_list_style_definition/
---

## List.is_list_style_definition property

Returns ``True`` if this list is a definition of a list style.



```python
@property
def is_list_style_definition(self) -> bool:
    ...

```

### Remarks

When this property is ``True``, the [List.style](../style/) property returns the list style that
this list defines.

By modifying properties of a list that defines a list style, you modify the properties
of the list style.

A list that is a definition of a list style cannot be applied directly to paragraphs
to make them numbered.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
# Podemos contener un objeto List completo dentro de un estilo.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Cambie la apariencia de todos los niveles de la lista en nuestra lista.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Cree otra lista a partir de una lista dentro de un estilo.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Agregue algunos elementos de lista que nuestra lista formateará.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Cree y aplique otra lista basada en el estilo de lista.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)
* property [List.style](../style/)
* property [List.is_list_style_reference](../is_list_style_reference/)

