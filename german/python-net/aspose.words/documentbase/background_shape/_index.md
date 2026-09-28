---
title: DocumentBase.background_shape property
linktitle: background_shape property
articleTitle: background_shape property
second_title: Aspose.Words for Python
description: "DocumentBase.background_shape property. Gets or sets the background shape of the document"
type: docs
weight: 10
url: /de/python-net/aspose.words/documentbase/background_shape/
---

## DocumentBase.background_shape property

Gets or sets the background shape of the document. Can be ``None``.



```python
@property
def background_shape(self) -> aspose.words.drawing.Shape:
    ...

@background_shape.setter
def background_shape(self, value: aspose.words.drawing.Shape):
    ...

```

### Remarks

Microsoft Word allows only a shape that has its [ShapeBase.shape_type](../../../aspose.words.drawing/shapebase/shape_type/) property equal
to [ShapeType.RECTANGLE](../../../aspose.words.drawing/shapetype/#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties
are ignored.

Setting this property to a non-null value will also set the [ViewOptions.display_background_shape](../../../aspose.words.settings/viewoptions/display_background_shape/) to ``True``.




### Examples

Shows how to set a background shape for every page of a document.

```python
doc = aw.Document()
self.assertIsNone(doc.background_shape)
# Der einzige Formtyp, den wir als Hintergrund verwenden können, ist ein Rechteck.
shape_rectangle = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
# Es gibt zwei Möglichkeiten, diese Form als Seitenhintergrund zu verwenden.
# 1 -  Eine einfarbige Farbe:
shape_rectangle.fill_color = aspose.pydrawing.Color.light_blue
doc.background_shape = shape_rectangle
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.BackgroundShape.FlatColor.docx')
# 2 -  Ein Bild:
shape_rectangle = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape_rectangle.image_data.set_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# Passen Sie das Erscheinungsbild des Bildes an, um es besser als Wasserzeichen zu verwenden.
shape_rectangle.image_data.contrast = 0.2
shape_rectangle.image_data.brightness = 0.7
doc.background_shape = shape_rectangle
self.assertTrue(doc.background_shape.has_image)
save_options = aw.saving.PdfSaveOptions()
save_options.cache_background_graphics = False
# Microsoft Word unterstützt keine Formen mit Bildern als Hintergründen,
# Aber wir können diese Hintergründe immer noch in anderen Speicherformaten wie .pdf sehen.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.BackgroundShape.Image.pdf', save_options=save_options)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* property [ViewOptions.display_background_shape](../../../aspose.words.settings/viewoptions/display_background_shape/)
* property [DocumentBase.page_color](../page_color/)

