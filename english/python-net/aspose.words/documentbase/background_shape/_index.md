---
title: DocumentBase.background_shape property
linktitle: background_shape property
articleTitle: background_shape property
second_title: Aspose.Words for Python
description: "DocumentBase.background_shape property. Gets or sets the background shape of the document"
type: docs
weight: 10
url: /python-net/aspose.words/documentbase/background_shape/
---

## DocumentBase.background_shape property

Gets or sets the background shape of the document. Can be ``None``.


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

# The only shape type that we can use as a background is a rectangle.
shape_rectangle = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)

# There are two ways of using this shape as a page background.
# 1 -  A flat color:
shape_rectangle.fill_color = drawing.Color.light_blue
doc.background_shape = shape_rectangle

doc.save(ARTIFACTS_DIR + "DocumentBase.background_shape.flat_color.docx")

# 2 -  An image:
shape_rectangle = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape_rectangle.image_data.set_image(IMAGE_DIR + "Transparent background logo.png")

# Adjust the image's appearance to make it more suitable as a watermark.
shape_rectangle.image_data.contrast = 0.2
shape_rectangle.image_data.brightness = 0.7

doc.background_shape = shape_rectangle

self.assertTrue(doc.background_shape.has_image)

save_options = aws.PdfSaveOptions()
save_options.cache_background_graphics = False
# Microsoft Word does not support shapes with images as backgrounds,
# but we can still see these backgrounds in other save formats such as .pdf.
doc.save(ARTIFACTS_DIR + "DocumentBase.background_shape.image.pdf", save_options)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* property [ViewOptions.display_background_shape](../../../aspose.words.settings/viewoptions/display_background_shape/)
* property [DocumentBase.page_color](../page_color/)

