---
title: ConvertUtil.pixel_to_point method
linktitle: pixel_to_point method
articleTitle: pixel_to_point method
second_title: Aspose.Words for Python
description: "aspose.words.ConvertUtil.pixel_to_point method"
type: docs
weight: 40
url: /fr/python-net/aspose.words/convertutil/pixel_to_point/
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
# Le "Page Setup" d'une section définit la taille des marges de la page en points.
# Nous pouvons également utiliser la classe "ConvertUtil" pour employer une unité de mesure différente,
# comme les pixels lors de la définition des limites.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100)
page_setup.bottom_margin = aw.ConvertUtil.pixel_to_point(pixels=200)
page_setup.left_margin = aw.ConvertUtil.pixel_to_point(pixels=225)
page_setup.right_margin = aw.ConvertUtil.pixel_to_point(pixels=125)
# Un pixel vaut 0,75 point.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
self.assertEqual(1, aw.ConvertUtil.point_to_pixel(points=0.75))
# La valeur DPI par défaut utilisée est 96.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1, resolution=96))
# Ajoutez du contenu pour démontrer les nouvelles marges.
builder.writeln(f'This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.left_margin)} pixels from the left, ' + f'{page_setup.right_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.right_margin)} pixels from the right, ' + f'{page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin)} pixels from the top, ' + f'and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.bottom_margin)} pixels from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixels.docx')
```

Shows how to use convert points to pixels with default and custom resolution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Définissez la taille de la marge supérieure de cette section en pixels, selon un DPI personnalisé.
my_dpi = 192
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100, resolution=my_dpi)
self.assertAlmostEqual(37.5, page_setup.top_margin, delta=0.01)
# À la résolution DPI par défaut de 96, un pixel vaut 0,75 point.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
builder.writeln(f'This Text is {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + f'pixels (at a DPI of {my_dpi}) from the top of the page.')
# Définissez un nouveau DPI et ajustez la valeur de la marge supérieure en conséquence.
new_dpi = 300
page_setup.top_margin = aw.ConvertUtil.pixel_to_new_dpi(page_setup.top_margin, my_dpi, new_dpi)
self.assertAlmostEqual(59, page_setup.top_margin, delta=0.01)
builder.writeln(f'At a DPI of {new_dpi}, the text is now {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + 'pixels from the top of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixelsDpi.docx')
```

## See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

