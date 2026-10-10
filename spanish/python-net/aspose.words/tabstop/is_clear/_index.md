---
title: TabStop.is_clear property
linktitle: is_clear property
articleTitle: is_clear property
second_title: Aspose.Words for Python
description: "TabStop.is_clear property. Returns ``True`` if this tab stop clears any existing tab stops in this position."
type: docs
weight: 30
url: /es/python-net/aspose.words/tabstop/is_clear/
---

## TabStop.is_clear property

Returns ``True`` if this tab stop clears any existing tab stops in this position.



```python
@property
def is_clear(self) -> bool:
    ...

```

### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 puntos equivalen a una "pulgada" en la regla de tabulaciones de Microsoft Word.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Cada carácter de "tab" lleva el cursor del constructor a la ubicación de la siguiente parada de tabulación.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Cada párrafo obtiene su colección de paradas de tabulación, que clona sus valores de la colección de paradas de tabulación del constructor de documentos.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# Una colección de paradas de tabulación puede señalarnos TabStops antes y después de ciertas posiciones.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Podemos borrar la colección de paradas de tabulación de un párrafo para volver al comportamiento de tabulación predeterminado.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStop](../)

