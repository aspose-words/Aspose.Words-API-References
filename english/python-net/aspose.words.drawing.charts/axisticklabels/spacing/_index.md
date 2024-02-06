---
title: AxisTickLabels.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for Python
description: "AxisTickLabels.spacing property. Gets or sets the interval at which the tick labels are drawn."
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/axisticklabels/spacing/
---

## AxisTickLabels.spacing property

Gets or sets the interval at which the tick labels are drawn.


```python
@property
def spacing(self) -> int:
    ...

@spacing.setter
def spacing(self, value: int):
    ...

```

### Remarks

The property has effect for text category and series axes. It is not supported by MS Office 2016 
new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [AxisTickLabels.is_auto_spacing](../is_auto_spacing/) property to ``False``.




### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisTickLabels](../)

