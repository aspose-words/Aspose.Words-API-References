---
title: TabStopCollection.remove_by_index method
linktitle: remove_by_index method
articleTitle: remove_by_index method
second_title: Aspose.Words for Python
description: "TabStopCollection.remove_by_index method. Removes a tab stop at the specified index from the collection."
type: docs
weight: 100
url: /python-net/aspose.words/tabstopcollection/remove_by_index/
---

## remove_by_index(index) {#int}

Removes a tab stop at the specified index from the collection.


```python
def remove_by_index(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

### Examples

Shows how to select a tab stop in a document by its index and remove it.

```python
doc = aw.Document()
tab_stops = doc.first_section.body.paragraphs[0].paragraph_format.tab_stops
tab_stops.add(aw.ConvertUtil.millimeter_to_point(30), aw.TabAlignment.LEFT, aw.TabLeader.DASHES)
tab_stops.add(aw.ConvertUtil.millimeter_to_point(60), aw.TabAlignment.LEFT, aw.TabLeader.DASHES)
self.assertEqual(2, tab_stops.count)
# Remove the first tab stop.
tab_stops.remove_by_index(0)
self.assertEqual(1, tab_stops.count)
doc.save(ARTIFACTS_DIR + 'TabStopCollection.remove_by_index.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

