---
title: ConvertUtil.pixel_to_point method
linktitle: pixel_to_point method
articleTitle: pixel_to_point method
second_title: Aspose.Words for Python
description: "aspose.words.ConvertUtil.pixel_to_point method"
type: docs
weight: 40
url: /it/python-net/aspose.words/convertutil/pixel_to_point/
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
# Il "Page Setup" di una sezione definisce la dimensione dei margini della pagina in punti.
# Possiamo anche utilizzare la classe "ConvertUtil" per usare un'unità di misura diversa,
# come i pixel quando si definiscono i confini.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100)
page_setup.bottom_margin = aw.ConvertUtil.pixel_to_point(pixels=200)
page_setup.left_margin = aw.ConvertUtil.pixel_to_point(pixels=225)
page_setup.right_margin = aw.ConvertUtil.pixel_to_point(pixels=125)
# Un pixel è pari a 0,75 punti.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
self.assertEqual(1, aw.ConvertUtil.point_to_pixel(points=0.75))
# Il valore DPI predefinito utilizzato è 96.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1, resolution=96))
# Aggiungi contenuto per dimostrare i nuovi margini.
builder.writeln(f'This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.left_margin)} pixels from the left, ' + f'{page_setup.right_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.right_margin)} pixels from the right, ' + f'{page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin)} pixels from the top, ' + f'and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.bottom_margin)} pixels from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixels.docx')
```

Shows how to use convert points to pixels with default and custom resolution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Definisci la dimensione del margine superiore di questa sezione in pixel, secondo un DPI personalizzato.
my_dpi = 192
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.pixel_to_point(pixels=100, resolution=my_dpi)
self.assertAlmostEqual(37.5, page_setup.top_margin, delta=0.01)
# Con il DPI predefinito di 96, un pixel corrisponde a 0,75 punti.
self.assertEqual(0.75, aw.ConvertUtil.pixel_to_point(pixels=1))
builder.writeln(f'This Text is {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + f'pixels (at a DPI of {my_dpi}) from the top of the page.')
# Imposta un nuovo DPI e regola di conseguenza il valore del margine superiore.
new_dpi = 300
page_setup.top_margin = aw.ConvertUtil.pixel_to_new_dpi(page_setup.top_margin, my_dpi, new_dpi)
self.assertAlmostEqual(59, page_setup.top_margin, delta=0.01)
builder.writeln(f'At a DPI of {new_dpi}, the text is now {page_setup.top_margin} points/{aw.ConvertUtil.point_to_pixel(points=page_setup.top_margin, resolution=my_dpi)} ' + 'pixels from the top of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndPixelsDpi.docx')
```

## See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

