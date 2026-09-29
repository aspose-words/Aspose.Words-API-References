---
title: TabStop.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "TabStop.equals method. Compares with the specified [TabStop](../)."
type: docs
weight: 60
url: /sv/python-net/aspose.words/tabstop/equals/
---

## equals(rhs) {#tabstop}

Compares with the specified [TabStop](../).



```python
def equals(self, rhs: aspose.words.TabStop):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [TabStop](../) |  |

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
* class [TabStop](../)

