---
title: TabStop constructor
linktitle: TabStop constructor
articleTitle: TabStop constructor
second_title: Aspose.Words for Python
description: "aspose.words.TabStop constructor"
type: docs
weight: 10
url: /it/python-net/aspose.words/tabstop/__init__/
---

## TabStop(position) {#float}

Initializes a new instance of this class.


```python
def __init__(self, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float |  |

## TabStop(position, alignment, leader) {#float_tabalignment_tableader}

Initializes a new instance of this class.


```python
def __init__(self, position: float, alignment: aspose.words.TabAlignment, leader: aspose.words.TabLeader):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float | The position of the tab stop in points. |
| alignment | [TabAlignment](../../tabalignment/) | A [TabAlignment](../../tabalignment/) value that specifies the alignment of text at this tab stop. |
| leader | [TabLeader](../../tableader/) | A [TabLeader](../../tableader/) value that specifies the type of the leader line displayed under the tab character. |

## Examples

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

## See Also

* module [aspose.words](../../)
* class [TabStop](../)

