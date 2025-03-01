﻿---
title: TabStopCollection.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "TabStopCollection.equals method. Determines whether the specified [TabStopCollection](../) is equal in value to the current [TabStopCollection](../)."
type: docs
weight: 70
url: /python-net/aspose.words/tabstopcollection/equals/
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
# 72 points is one "inch" on the Microsoft Word tab stop ruler.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# A tab stop collection can point us to TabStops before and after certain positions.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

