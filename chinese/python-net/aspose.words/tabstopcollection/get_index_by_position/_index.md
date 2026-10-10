---
title: TabStopCollection.get_index_by_position method
linktitle: get_index_by_position method
articleTitle: get_index_by_position method
second_title: Aspose.Words for Python
description: "TabStopCollection.get_index_by_position method. Gets the index of a tab stop with the specified position in points."
type: docs
weight: 80
url: /zh/python-net/aspose.words/tabstopcollection/get_index_by_position/
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
# 在 30 毫米的位置添加一个制表位。
tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(30), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# "GetIndexByPosition" 返回的结果为 "0"，确认存在一个制表位
# 位于 30 毫米的制表位存在于此集合中，且索引为 0。
self.assertEqual(0, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(30)))
# "GetIndexByPosition" 返回 "-1"，确认
# 此集合中没有位置为 60 毫米的制表位。
self.assertEqual(-1, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(60)))
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

