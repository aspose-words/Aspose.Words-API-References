---
title: ConvertUtil.pixel_to_point method
linktitle: pixel_to_point method
articleTitle: pixel_to_point method
second_title: Aspose.Words for Python
description: "aspose.words.ConvertUtil.pixel_to_point method"
type: docs
weight: 40
url: /zh/python-net/aspose.words/convertutil/pixel_to_point/
---

## pixel_to_point(pixels) {#float}

Converts pixels to points at 96 dpi.


```python
def pixel_to_point(self, pixels: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pixels | float | The value to convert. |

### Remarks

1 inch equals 72 points.


## pixel_to_point(pixels, resolution) {#float_float}

Converts pixels to points at the specified pixel resolution.


```python
def pixel_to_point(self, pixels: float, resolution: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pixels | float | The value to convert. |
| resolution | float | The dpi (dots per inch) resolution. |

### Remarks

1 inch equals 72 points.


## Examples

Shows how to specify page properties in pixels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 节的“页面设置”定义了页面边距的大小（单位为点）。
# 我们也可以使用 "ConvertUtil" 类来使用不同的测量单位，
# 例如在定义边界时使用像素。
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100)
page_setup.bottom_margin = aw.ConvertUtil.pixel_to_point(pixels=200)
page_setup.left_margin = aw.ConvertUtil.pixel_to_point(pixels=225)
page_setup.right_margin = aw.ConvertUtil.pixel_to_point(pixels=125)
# 像素等于 0.75 点。
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
self.assertEqual(1, aw.ConvertUtil.point_to_pixel(points=0.75))
# 使用的默认 DPI 值为 96。
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1, resolution=96))
# 添加内容以演示新的边距。
builder.writeln(f'This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.left_margin)} pixels from the left, ' + f'{page_setup.right_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.right_margin)} pixels from the right, ' + f'{page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin)} pixels from the top, ' + f'and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.bottom_margin)} pixels from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixels.docx')
```

Shows how to use convert points to pixels with default and custom resolution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 根据自定义 DPI，定义本节顶部边距的像素大小。
my_dpi = 192
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100, resolution=my_dpi)
self.assertAlmostEqual(37.5, page_setup.top_margin, delta=0.01)
# 在默认 DPI 96 下，像素等于 0.75 点。
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
builder.writeln(f'This Text is {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + f'pixels (at a DPI of {my_dpi}) from the top of the page.')
# 设置新的 DPI 并相应地调整顶部边距的数值。
new_dpi = 300
page_setup.top_margin = aw.ConvertUtil.pixel_to_new_dpi(page_setup.top_margin, my_dpi, new_dpi)
self.assertAlmostEqual(59, page_setup.top_margin, delta=0.01)
builder.writeln(f'At a DPI of {new_dpi}, the text is now {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + 'pixels from the top of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixelsDpi.docx')
```

## See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

