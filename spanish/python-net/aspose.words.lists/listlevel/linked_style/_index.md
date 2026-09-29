---
title: ListLevel.linked_style property
linktitle: linked_style property
articleTitle: linked_style property
second_title: Aspose.Words for Python
description: "ListLevel.linked_style property. Gets or sets the paragraph style that is linked to this list level."
type: docs
weight: 60
url: /es/python-net/aspose.words.lists/listlevel/linked_style/
---

## ListLevel.linked_style property

Gets or sets the paragraph style that is linked to this list level.


```python
@property
def linked_style(self) -> aspose.words.Style:
    ...

@linked_style.setter
def linked_style(self, value: aspose.words.Style):
    ...

```

### Remarks

This property is ``None`` when the list level is not linked to a paragraph style.
This property can be set to ``None``.




### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Las etiquetas de nivel 1 se formatearán según el estilo de párrafo "Heading 1" y tendrán un prefijo.
# Estas se verán como "Appendix A", "Appendix B"...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# Las etiquetas de nivel 2 mostrarán los números actuales del primer y segundo nivel de lista y tendrán ceros iniciales.
# Si el primer nivel de lista está en 1, entonces las etiquetas de lista se verán como "Section (1.01)", "Section (1.02)"...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# Observe que el nivel superior utiliza numeración UppercaseLetter.
# Podemos establecer la propiedad "IsLegal" para usar números arábigos en los niveles superiores de la lista.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# Las etiquetas de nivel 3 serán números romanos en mayúsculas con un prefijo y un sufijo y se reiniciarán en cada elemento de nivel 1 de la lista.
# Estas etiquetas de lista se verán como "-I-", "-II-"...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# Haz que las etiquetas de todos los niveles de lista estén en negrita.
for level in doc_list.list_levels:
    level.font.bold = True
# Aplica el formato de lista al párrafo actual.
builder.list_format.list = doc_list
# Crea elementos de lista que mostrarán los tres niveles de nuestra lista.
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

