---
title: Chart.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "Chart.source_full_name property. Gets the path and name of an xls/xlsx file this chart is linked to."
type: docs
weight: 100
url: /python-net/aspose.words.drawing.charts/chart/source_full_name/
---

## Chart.source_full_name property

Gets the path and name of an xls/xlsx file this chart is linked to.


```python
@property
def source_full_name(self) -> str:
    ...

@source_full_name.setter
def source_full_name(self, value: str):
    ...

```

### Examples

Shows how to get/set the full name of the external xls/xlsx document if the chart is linked.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape with linked chart.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
source_full_name = shape.chart.source_full_name
self.assertTrue('Examples\\Data\\Spreadsheet.xlsx' in source_full_name)
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

