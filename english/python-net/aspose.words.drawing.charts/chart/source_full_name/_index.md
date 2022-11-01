---
title: source_full_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the path and name of an xls/xlsx file this chart is linked to."
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chart/source_full_name/
---

## Chart.source_full_name property

Gets the path and name of an xls/xlsx file this chart is linked to.


### Examples

Shows how to get the full name of the external xls/xlsx document if the chart is linked.

```python
doc = aw.Document(MY_DIR + "Shape with linked chart.docx")

shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

self.assertIn("Examples\\Data\\Spreadsheet.xlsx", shape.chart.source_full_name)
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

