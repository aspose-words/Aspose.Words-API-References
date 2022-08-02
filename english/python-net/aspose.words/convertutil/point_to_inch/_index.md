---
title: point_to_inch method
second_title: Aspose.Words for Python via .NET API Reference
description: "Converts points to inches."
type: docs
weight: 50
url: /python-net/aspose.words/convertutil/point_to_inch/
---

## point_to_inch(points) {#float}

Converts points to inches.


```python
def point_to_inch(self, points: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | float |  |

1 inch equals 72 points.


### Examples

Shows how to specify page properties in inches.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A section's "Page Setup" defines the size of the page margins in points.
# We can also use the "ConvertUtil" class to use a more familiar measurement unit,
# such as inches when defining boundaries.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.inch_to_point(1.0)
page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(2.0)
page_setup.left_margin = aw.ConvertUtil.inch_to_point(2.5)
page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)

# An inch is 72 points.
self.assertEqual(72.0, aw.ConvertUtil.inch_to_point(1))
self.assertEqual(1.0, aw.ConvertUtil.point_to_inch(72))

# Add content to demonstrate the new margins.
builder.writeln(
    f"This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.left_margin)} inches from the left, " +
    f"{page_setup.right_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.right_margin)} inches from the right, " +
    f"{page_setup.top_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.top_margin)} inches from the top, " +
    f"and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.bottom_margin)} inches from the bottom of the page.")

doc.save(ARTIFACTS_DIR + "UtilityClasses.points_and_inches.docx")
```

### See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

