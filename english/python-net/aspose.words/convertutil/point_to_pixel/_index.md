---
title: ConvertUtil.point_to_pixel method
linktitle: point_to_pixel method
articleTitle: point_to_pixel method
second_title: Aspose.Words for Python
description: "aspose.words.ConvertUtil.point_to_pixel method"
type: docs
weight: 60
url: /python-net/aspose.words/convertutil/point_to_pixel/
---

## point_to_pixel(points) {#float}

Converts points to pixels at 96 dpi.


```python
def point_to_pixel(self, points: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | float | The value to convert. |

### Remarks

1 inch equals 72 points.


## point_to_pixel(points, resolution) {#float_float}

Converts points to pixels at the specified pixel resolution.


```python
def point_to_pixel(self, points: float, resolution: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | float | The value to convert. |
| resolution | float | The dpi (dots per inch) resolution. |

### Remarks

1 inch equals 72 points.


## Examples

Shows how to specify page properties in pixels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# A section's "Page Setup" defines the size of the page margins in points.
# We can also use the "ConvertUtil" class to use a different measurement unit,
# such as pixels when defining boundaries.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100)
page_setup.bottom_margin = aw.ConvertUtil.pixel_to_point(pixels=200)
page_setup.left_margin = aw.ConvertUtil.pixel_to_point(pixels=225)
page_setup.right_margin = aw.ConvertUtil.pixel_to_point(pixels=125)
# A pixel is 0.75 points.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
self.assertEqual(1, aw.ConvertUtil.point_to_pixel(points=0.75))
# The default DPI value used is 96.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1, resolution=96))
# Add content to demonstrate the new margins.
builder.writeln(f'This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.left_margin)} pixels from the left, ' + f'{page_setup.right_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.right_margin)} pixels from the right, ' + f'{page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin)} pixels from the top, ' + f'and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.bottom_margin)} pixels from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixels.docx')
```

Shows how to use convert points to pixels with default and custom resolution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Define the size of the top margin of this section in pixels, according to a custom DPI.
my_dpi = 192
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100, resolution=my_dpi)
self.assertAlmostEqual(37.5, page_setup.top_margin, delta=0.01)
# At the default DPI of 96, a pixel is 0.75 points.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
builder.writeln(f'This Text is {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + f'pixels (at a DPI of {my_dpi}) from the top of the page.')
# Set a new DPI and adjust the top margin value accordingly.
new_dpi = 300
page_setup.top_margin = aw.ConvertUtil.pixel_to_new_dpi(page_setup.top_margin, my_dpi, new_dpi)
self.assertAlmostEqual(59, page_setup.top_margin, delta=0.01)
builder.writeln(f'At a DPI of {new_dpi}, the text is now {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + 'pixels from the top of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixelsDpi.docx')
```

## See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

