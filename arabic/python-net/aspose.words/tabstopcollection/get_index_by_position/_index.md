---
title: TabStopCollection.get_index_by_position method
linktitle: get_index_by_position method
articleTitle: get_index_by_position method
second_title: Aspose.Words for Python
description: "TabStopCollection.get_index_by_position method. Gets the index of a tab stop with the specified position in points."
type: docs
weight: 80
url: /ar/python-net/aspose.words/tabstopcollection/get_index_by_position/
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
# أضف نقطة تبويب في موضع 30 مم.
tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(30), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# نتيجة "0" التي تُرجعها "GetIndexByPosition" تؤكد أن نقطة تبويب
# في 30 مم موجودة في هذه المجموعة، وهي في الفهرس 0.
self.assertEqual(0, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(30)))
# قيمة "-1" التي تُرجعها "GetIndexByPosition" تؤكد أن
# لا توجد نقطة تبويب في هذه المجموعة بموضع 60 مم.
self.assertEqual(-1, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(60)))
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

