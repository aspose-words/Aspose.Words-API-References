---
title: MultiPageLayout.grid method
linktitle: grid method
articleTitle: grid method
second_title: Aspose.Words for Python
description: "MultiPageLayout.grid method. Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns."
type: docs
weight: 40
url: /python-net/aspose.words.saving/multipagelayout/grid/
---

## grid(columns, horizontal_gap, vertical_gap) {#int_float_float}

Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the
specified number of columns.


```python
def grid(self, columns: int, horizontal_gap: float, vertical_gap: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| columns | int | The number of columns in the layout. Must be greater than zero. |
| horizontal_gap | float | The horizontal gap between columns in points. |
| vertical_gap | float | The vertical gap between rows in points. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Thrown if *columns* is less than or equal to zero. |

### See Also

* module [aspose.words.saving](../../)
* class [MultiPageLayout](../)

