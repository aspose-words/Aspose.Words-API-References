---
title: ConvertUtil.millimeter_to_point method
linktitle: millimeter_to_point method
articleTitle: millimeter_to_point method
second_title: Aspose.Words for Python
description: "ConvertUtil.millimeter_to_point method. Converts millimeters to points."
type: docs
weight: 20
url: /python-net/aspose.words/convertutil/millimeter_to_point/
---

## millimeter_to_point(millimeters) {#float}

Converts millimeters to points.


```python
def millimeter_to_point(self, millimeters: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | float | The value to convert. |

### Remarks

1 inch equals 25.4 millimeters. 1 inch equals 72 points.


### Examples

Shows how to specify page properties in millimeters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# A section's "Page Setup" defines the size of the page margins in points.
# We can also use the "ConvertUtil" class to use a more familiar measurement unit,
# such as millimeters when defining boundaries.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.millimeter_to_point(30)
page_setup.bottom_margin = aw.ConvertUtil.millimeter_to_point(50)
page_setup.left_margin = aw.ConvertUtil.millimeter_to_point(80)
page_setup.right_margin = aw.ConvertUtil.millimeter_to_point(40)
# A centimeter is approximately 28.3 points.
self.assertAlmostEqual(28.34, aw.ConvertUtil.millimeter_to_point(10), delta=0.01)
# Add content to demonstrate the new margins.
builder.writeln(f'This Text is {page_setup.left_margin} points from the left, ' + f'{page_setup.right_margin} points from the right, ' + f'{page_setup.top_margin} points from the top, ' + f'and {page_setup.bottom_margin} points from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndMillimeters.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

