---
title: TabStop.is_clear property
linktitle: is_clear property
articleTitle: is_clear property
second_title: Aspose.Words for Python
description: "TabStop.is_clear property. Returns ``True`` if this tab stop clears any existing tab stops in this position."
type: docs
weight: 30
url: /it/python-net/aspose.words/tabstop/is_clear/
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
# 72 punti corrispondono a un "pollice" sul righello dei tab di Microsoft Word.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Ogni carattere "tab" porta il cursore del builder alla posizione della tabulazione successiva.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Ogni paragrafo ottiene la sua raccolta di tabulazioni, che clona i suoi valori dalla raccolta di tabulazioni del document builder.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# Una raccolta di tabulazioni può indicarci i TabStops prima e dopo certe posizioni.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Possiamo cancellare la raccolta di tabulazioni di un paragrafo per tornare al comportamento di tabulazione predefinito.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStop](../)

