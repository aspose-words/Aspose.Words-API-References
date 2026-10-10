---
title: TabStopCollection.before method
linktitle: before method
articleTitle: before method
second_title: Aspose.Words for Python
description: "TabStopCollection.before method. Gets a first tab stop to the left of the specified position."
type: docs
weight: 50
url: /fr/python-net/aspose.words/tabstopcollection/before/
---

## before(position) {#float}

Gets a first tab stop to the left of the specified position.


```python
def before(self, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float | The reference position (in points). |

### Remarks

Skips tab stops with [TabStop.alignment](../../tabstop/alignment/) set to [TabAlignment.BAR](../../tabalignment/#BAR).




### Returns

A tab stop object or ``None`` if a suitable tab stop was not found.


### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 points correspondent à un \"pouce\" sur la règle de tabulation de Microsoft Word.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Chaque caractère \"tab\" déplace le curseur du constructeur vers l'emplacement de l'arrêt de tabulation suivant.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Chaque paragraphe obtient sa collection d'arrêts de tabulation, qui clone ses valeurs à partir de la collection d'arrêts de tabulation du constructeur de document.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# Une collection d'arrêts de tabulation peut nous indiquer les TabStops avant et après certaines positions.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Nous pouvons effacer la collection d'arrêts de tabulation d'un paragraphe pour revenir au comportement de tabulation par défaut.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

