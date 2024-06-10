---
title: TabStopCollection.get_position_by_index method
linktitle: get_position_by_index method
articleTitle: get_position_by_index method
second_title: Aspose.Words for Python
description: "TabStopCollection.get_position_by_index method. Gets the position (in points) of the tab stop at the specified index."
type: docs
weight: 90
url: /python-net/aspose.words/tabstopcollection/get_position_by_index/
---

## get_position_by_index(index) {#int}

Gets the position (in points) of the tab stop at the specified index.


```python
def get_position_by_index(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

### Returns

The position of the tab stop.


### Examples

Shows how to find a tab, stop by its index and verify its position.

```python
doc = aw.Document()
tab_stops = doc.first_section.body.paragraphs[0].paragraph_format.tab_stops
tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(30), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(60), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# Verify the position of the second tab stop in the collection.
self.assertAlmostEqual(aw.ConvertUtil.millimeter_to_point(60), tab_stops.get_position_by_index(1), delta=0.1)
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

