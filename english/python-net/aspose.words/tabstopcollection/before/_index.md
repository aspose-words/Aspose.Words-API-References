---
title: TabStopCollection.before method
linktitle: before method
articleTitle: before method
second_title: Aspose.Words for Python
description: "TabStopCollection.before method. Gets a first tab stop to the left of the specified position."
type: docs
weight: 50
url: /python-net/aspose.words/tabstopcollection/before/
---

## before(position) {#float}

Gets a first tab stop to the left of the specified position.


```python
def before(self, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float |  |

Skips tab stops with [TabStop.alignment](../../tabstop/alignment/) set to [TabAlignment.BAR](../../tabalignment/#BAR).




### Returns

A tab stop object or ``None`` if a suitable tab stop was not found.


### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

tab_stops = builder.paragraph_format.tab_stops

# 72 points is one "inch" on the Microsoft Word tab stop ruler.
tab_stops.add(aw.TabStop(72.0))
tab_stops.add(aw.TabStop(432.0, aw.TabAlignment.RIGHT, aw.TabLeader.DASHES))

self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertNotEqual(tab_stops[0], tab_stops[1])

# Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder.writeln("Start\tTab 1\tTab 2")

paragraphs = doc.first_section.body.paragraphs

self.assertEqual(2, paragraphs.count)

# Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
#Assert.are_not_same(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)

# A tab stop collection can point us to tab_stops before and after certain positions.
self.assertEqual(72.0, tab_stops.before(100.0).position)
self.assertEqual(432.0, tab_stops.after(100.0).position)

# We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
paragraphs[1].paragraph_format.tab_stops.clear()

self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)

doc.save(ARTIFACTS_DIR + "TabStopCollection.tab_stop_collection.docx")
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

