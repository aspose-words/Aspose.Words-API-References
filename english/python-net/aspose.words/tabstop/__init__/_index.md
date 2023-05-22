---
title: TabStop constructor
linktitle: TabStop constructor
articleTitle: TabStop constructor
second_title: Aspose.Words for Python
description: "aspose.words.TabStop constructor"
type: docs
weight: 10
url: /python-net/aspose.words/tabstop/__init__/
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
| position | float |  |
| alignment | [TabAlignment](../../tabalignment/) |  |
| leader | [TabLeader](../../tableader/) |  |

## Examples

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

## See Also

* module [aspose.words](../../)
* class [TabStop](../)

