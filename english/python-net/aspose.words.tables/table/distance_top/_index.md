---
title: Table.distance_top property
linktitle: distance_top property
articleTitle: distance_top property
second_title: Aspose.Words for Python
description: "Table.distance_top property. Gets or sets distance between table top and the surrounding text, in points."
type: docs
weight: 150
url: /python-net/aspose.words.tables/table/distance_top/
---

## Table.distance_top property

Gets or sets distance between table top and the surrounding text, in points.


```python
@property
def distance_top(self) -> float:
    ...

@distance_top.setter
def distance_top(self, value: float):
    ...

```

### Examples

Shows how to set distance between table boundaries and text.

```python
doc = aw.Document(file_name=MY_DIR + 'Table wrapped by text.docx')
table = doc.first_section.body.tables[0]
self.assertEqual(25.9, table.distance_top)
self.assertEqual(25.9, table.distance_bottom)
self.assertEqual(17.3, table.distance_left)
self.assertEqual(17.3, table.distance_right)
# Set distance between table and surrounding text.
table.distance_left = 24
table.distance_right = 24
table.distance_top = 3
table.distance_bottom = 3
doc.save(file_name=ARTIFACTS_DIR + 'Table.DistanceBetweenTableAndText.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

