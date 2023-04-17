---
title: distance_bottom property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets distance between table bottom and the surrounding text, in points."
type: docs
weight: 120
url: /python-net/aspose.words.tables/table/distance_bottom/
---

## Table.distance_bottom property

Gets or sets distance between table bottom and the surrounding text, in points.


### Examples

Shows the minimum distance operations between table boundaries and text.

```python
doc = aw.Document(MY_DIR + "Table wrapped by text.docx")

table = doc.first_section.body.tables[0]

self.assertEqual(25.9, table.distance_top)
self.assertEqual(25.9, table.distance_bottom)
self.assertEqual(17.3, table.distance_left)
self.assertEqual(17.3, table.distance_right)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

