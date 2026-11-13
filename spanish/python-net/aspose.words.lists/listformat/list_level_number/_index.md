---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /es/python-net/aspose.words.lists/listformat/list_level_number/
---

## ListFormat.list_level_number property

Gets or sets the list level number (0 to 8) for the paragraph.


```python
@property
def list_level_number(self) -> int:
    ...

@list_level_number.setter
def list_level_number(self, value: int):
    ...

```

### Remarks

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [ListFormat.list](../list/) property is set to reference a valid list.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo e indentaciones.
# Podemos crear listas anidadas aumentando el nivel de indentación.
# Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
# Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
# A continuación se presentan dos tipos de listas que podemos crear con un generador de documentos.
# 1 -  Una lista con viñetas:
# Esta lista aplicará una indentación y un símbolo de viñeta ("•") antes de cada párrafo.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Finalizar la lista con viñetas.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  Una lista numerada:
# Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.list_format.apply_number_default()
# Este párrafo es el primer elemento. El primer elemento de una lista numerada tendrá un "1." como su símbolo de elemento de lista.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# Llame al método "ListIndent" para aumentar el nivel de lista actual,
# lo que iniciará una nueva lista autónoma, con una sangría más profunda, en el elemento actual del primer nivel de lista.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Estos son los primeros tres elementos de lista del segundo nivel de lista, que mantendrán un recuento
# independiente del recuento del primer nivel de lista. Según el formato de lista actual,
# tendrán símbolos de "a.", "b.", y "c.".
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# Llame al método "ListOutdent" para volver al nivel de lista anterior.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Estos dos párrafos continuarán el recuento del primer nivel de lista.
# Estos elementos tendrán símbolos de "2.", y "3."
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Si aumentamos el nivel de lista a un nivel al que ya habíamos añadido elementos anteriormente,
# la lista anidada será independiente de la anterior, y su numeración comenzará desde el principio.
# Estos elementos de lista tendrán símbolos de "a.", "b.", "c.", "d.", y "e".
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Desidenta el nivel de la lista nuevamente.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Finaliza la lista numerada.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

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

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)

