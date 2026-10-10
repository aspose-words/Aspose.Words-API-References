---
title: DocumentBase.background_shape property
linktitle: background_shape property
articleTitle: background_shape property
second_title: Aspose.Words for Python
description: "DocumentBase.background_shape property. Gets or sets the background shape of the document"
type: docs
weight: 10
url: /zh/python-net/aspose.words/documentbase/background_shape/
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
# 我们可以用作背景的唯一形状类型是矩形。
shape_rectangle = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
# 使用此形状作为页面背景有两种方式。
# 1 -  纯色：
shape_rectangle.fill_color = aspose.pydrawing.Color.light_blue
doc.background_shape = shape_rectangle
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.BackgroundShape.FlatColor.docx')
# 2 -  图片：
shape_rectangle = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape_rectangle.image_data.set_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# 调整图像的外观，使其更适合作为水印。
shape_rectangle.image_data.contrast = 0.2
shape_rectangle.image_data.brightness = 0.7
doc.background_shape = shape_rectangle
self.assertTrue(doc.background_shape.has_image)
save_options = aw.saving.PdfSaveOptions()
save_options.cache_background_graphics = False
# Microsoft Word 不支持以图像作为背景的形状，
# 但我们仍然可以在其他保存格式（例如 .pdf）中看到这些背景。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.BackgroundShape.Image.pdf', save_options=save_options)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* property [ViewOptions.display_background_shape](../../../aspose.words.settings/viewoptions/display_background_shape/)
* property [DocumentBase.page_color](../page_color/)

