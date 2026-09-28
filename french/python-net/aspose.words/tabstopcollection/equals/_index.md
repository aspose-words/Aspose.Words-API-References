---
title: TabStopCollection.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "TabStopCollection.equals method. Determines whether the specified [TabStopCollection](../) is equal in value to the current [TabStopCollection](../)."
type: docs
weight: 70
url: /fr/python-net/aspose.words/tabstopcollection/equals/
---

## equals(rhs) {#tabstopcollection}

Determines whether the specified [TabStopCollection](../) is equal in value to the current [TabStopCollection](../).



```python
def equals(self, rhs: aspose.words.TabStopCollection):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [TabStopCollection](../) |  |

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

