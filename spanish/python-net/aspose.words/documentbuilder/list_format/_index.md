---
title: DocumentBuilder.list_format property
linktitle: list_format property
articleTitle: list_format property
second_title: Aspose.Words for Python
description: "DocumentBuilder.list_format property. Returns an object that represents current list formatting properties."
type: docs
weight: 150
url: /es/python-net/aspose.words/documentbuilder/list_format/
---

## DocumentBuilder.list_format property

Returns an object that represents current list formatting properties.


```python
@property
def list_format(self) -> aspose.words.lists.ListFormat:
    ...

```

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

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

