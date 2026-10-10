---
title: TabStopCollection.get_index_by_position method
linktitle: get_index_by_position method
articleTitle: get_index_by_position method
second_title: Aspose.Words for Python
description: "TabStopCollection.get_index_by_position method. Gets the index of a tab stop with the specified position in points."
type: docs
weight: 80
url: /fr/python-net/aspose.words/tabstopcollection/get_index_by_position/
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
# Ajoutez une tabulation à une position de 30mm.
tab_stops.add(position=aw.ConvertUtil.millimeter_to_point(30), alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DASHES)
# Un résultat de "0" retourné par "GetIndexByPosition" confirme qu'une tabulation
# à 30mm existe dans cette collection, et elle se trouve à l'index 0.
self.assertEqual(0, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(30)))
# Un "-1" retourné par "GetIndexByPosition" confirme que
# il n'existe aucune tabulation dans cette collection avec une position de 60mm.
self.assertEqual(-1, tab_stops.get_index_by_position(aw.ConvertUtil.millimeter_to_point(60)))
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

