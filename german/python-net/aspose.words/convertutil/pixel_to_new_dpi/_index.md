---
title: ConvertUtil.pixel_to_new_dpi method
linktitle: pixel_to_new_dpi method
articleTitle: pixel_to_new_dpi method
second_title: Aspose.Words for Python
description: "ConvertUtil.pixel_to_new_dpi method. Converts pixels from one resolution to another."
type: docs
weight: 30
url: /de/python-net/aspose.words/convertutil/pixel_to_new_dpi/
---

## pixel_to_new_dpi(pixels, old_dpi, new_dpi) {#float_float_float}

Converts pixels from one resolution to another.


```python
def pixel_to_new_dpi(self, pixels: float, old_dpi: float, new_dpi: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pixels | float | The value to convert. |
| old_dpi | float | The current dpi (dots per inch) resolution. |
| new_dpi | float | The new dpi (dots per inch) resolution. |

### Examples

Shows how to use convert points to pixels with default and custom resolution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Definieren Sie die Größe des oberen Randes dieses Abschnitts in Pixeln, basierend auf einer benutzerdefinierten DPI.
my_dpi = 192
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100, resolution=my_dpi)
self.assertAlmostEqual(37.5, page_setup.top_margin, delta=0.01)
# Bei der Standard-DPI von 96 entspricht ein Pixel 0,75 Punkten.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
builder.writeln(f'This Text is {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + f'pixels (at a DPI of {my_dpi}) from the top of the page.')
# Legen Sie eine neue DPI fest und passen Sie den Wert des oberen Randes entsprechend an.
new_dpi = 300
page_setup.top_margin = aw.ConvertUtil.pixel_to_new_dpi(page_setup.top_margin, my_dpi, new_dpi)
self.assertAlmostEqual(59, page_setup.top_margin, delta=0.01)
builder.writeln(f'At a DPI of {new_dpi}, the text is now {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + 'pixels from the top of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixelsDpi.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

