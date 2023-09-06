﻿---
title: ConvertUtil class
linktitle: ConvertUtil class
articleTitle: ConvertUtil class
second_title: Aspose.Words for Python
description: "aspose.words.ConvertUtil class. Provides helper functions to convert between various measurement units"
type: docs
weight: 270
url: /python-net/aspose.words/convertutil/
---

## ConvertUtil class

Provides helper functions to convert between various measurement units.
To learn more, visit the [Convert Between Measurement Units](https://docs.aspose.com/words/python-net/convert-between-measurement-units/) documentation article.




### Methods

| Name | Description |
| --- | --- |
|[ inch_to_point(inches)](./inch_to_point/#float) | Converts inches to points. |
|[ millimeter_to_point(millimeters)](./millimeter_to_point/#float) | Converts millimeters to points. |
|[ pixel_to_new_dpi(pixels, old_dpi, new_dpi)](./pixel_to_new_dpi/#float_float_float) | Converts pixels from one resolution to another. |
|[ pixel_to_point(pixels)](./pixel_to_point/#float) | Converts pixels to points at 96 dpi. |
|[ pixel_to_point(pixels, resolution)](./pixel_to_point/#float_float) | Converts pixels to points at the specified pixel resolution. |
|[ point_to_inch(points)](./point_to_inch/#float) | Converts points to inches. |
|[ point_to_pixel(points)](./point_to_pixel/#float) | Converts points to pixels at 96 dpi. |
|[ point_to_pixel(points, resolution)](./point_to_pixel/#float_float) | Converts points to pixels at the specified pixel resolution. |

### Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.page_setup.paper_size = aw.PaperSize.LEGAL
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.top_margin = aw.ConvertUtil.inch_to_point(1.0)
builder.page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(1.0)
builder.page_setup.left_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.header_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.page_setup.footer_distance = aw.ConvertUtil.inch_to_point(0.2)

builder.writeln("Hello world!")

doc.save(ARTIFACTS_DIR + "PageSetup.page_margins.docx")
```

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

* module [aspose.words](../)

