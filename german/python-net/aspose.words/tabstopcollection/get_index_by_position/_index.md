---
title: TabStopCollection.get_index_by_position method
linktitle: get_index_by_position method
articleTitle: get_index_by_position method
second_title: Aspose.Words for Python
description: "TabStopCollection.get_index_by_position method. Gets the index of a tab stop with the specified position in points."
type: docs
weight: 80
url: /de/python-net/aspose.words/tabstopcollection/get_index_by_position/
---

## get_index_by_position(position) {#float}

Gets the index of a tab stop with the specified position in points.


```python
def get_index_by_position(self, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float |  |

### Examples

Shows how to look up a position to see if a tab stop exists there and obtain its index.

```python
doc = aw.Document()
tab_stops = doc.first_section.body.paragraphs[0].paragraph_format.tab_stops
# Fügen Sie einen Tabstopp an der Position von 30 mm hinzu.
tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(30), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# Ein Ergebnis von "0", das von "GetIndexByPosition" zurückgegeben wird, bestätigt, dass ein Tabstopp
# bei 30 mm in dieser Sammlung existiert und sich an Index 0 befindet.
self.assertEqual(0, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(30)))
# Ein "-1", das von "GetIndexByPosition" zurückgegeben wird, bestätigt, dass
# in dieser Sammlung kein Tabstopp mit einer Position von 60 mm vorhanden ist.
self.assertEqual(-1, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(60)))
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

