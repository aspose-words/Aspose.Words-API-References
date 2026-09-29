---
title: ConvertUtil.point_to_pixel method
linktitle: point_to_pixel method
articleTitle: point_to_pixel method
second_title: Aspose.Words for Python
description: "aspose.words.ConvertUtil.point_to_pixel method"
type: docs
weight: 60
url: /sv/python-net/aspose.words/convertutil/point_to_pixel/
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
# En sektions "Page Setup" definierar storleken på sidmarginalerna i punkter.
# Vi kan också använda klassen "ConvertUtil" för att använda en annan mätenhet,
# såsom pixlar när vi definierar gränser.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100)
page_setup.bottom_margin = aw.ConvertUtil.pixel_to_point(pixels=200)
page_setup.left_margin = aw.ConvertUtil.pixel_to_point(pixels=225)
page_setup.right_margin = aw.ConvertUtil.pixel_to_point(pixels=125)
# En pixel är 0,75 punkter.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
self.assertEqual(1, aw.ConvertUtil.point_to_pixel(points=0.75))
# Standard‑DPI‑värdet som används är 96.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1, resolution=96))
# Lägg till innehåll för att demonstrera de nya marginalerna.
builder.writeln(f'This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.left_margin)} pixels from the left, ' + f'{page_setup.right_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.right_margin)} pixels from the right, ' + f'{page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin)} pixels from the top, ' + f'and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.bottom_margin)} pixels from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixels.docx')
```

Shows how to use convert points to pixels with default and custom resolution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Definiera storleken på den övre marginalen för detta avsnitt i pixlar, enligt en anpassad DPI.
my_dpi = 192
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100, resolution=my_dpi)
self.assertAlmostEqual(37.5, page_setup.top_margin, delta=0.01)
# Vid standard‑DPI på 96 är en pixel 0,75 punkter.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
builder.writeln(f'This Text is {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + f'pixels (at a DPI of {my_dpi}) from the top of the page.')
# Ställ in ett nytt DPI och justera värdet för den övre marginalen därefter.
new_dpi = 300
page_setup.top_margin = aw.ConvertUtil.pixel_to_new_dpi(page_setup.top_margin, my_dpi, new_dpi)
self.assertAlmostEqual(59, page_setup.top_margin, delta=0.01)
builder.writeln(f'At a DPI of {new_dpi}, the text is now {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + 'pixels from the top of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixelsDpi.docx')
```

## See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

