---
title: TabStopCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "TabStopCollection.count property. Gets the number of tab stops in the collection."
type: docs
weight: 20
url: /sv/python-net/aspose.words/tabstopcollection/count/
---

## TabStopCollection.count property

Gets the number of tab stops in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 punkter är en \"tum\" på Microsoft Word-tabbstopp‑linjalen.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Varje \"tab\"-tecken flyttar byggarens markör till platsen för nästa tabbstopp.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Varje stycke får sin tabbstopp‑samling, som klonar sina värden från dokumentbyggarens tabbstopp‑samling.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# En tabbstopp‑samling kan peka oss till TabStops före och efter vissa positioner.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Vi kan rensa ett styckes tabbstopp‑samling för att återgå till standardtabb‑beteendet.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

