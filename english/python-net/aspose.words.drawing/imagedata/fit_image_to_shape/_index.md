---
title: ImageData.fit_image_to_shape method
linktitle: fit_image_to_shape method
articleTitle: fit_image_to_shape method
second_title: Aspose.Words for Python
description: "ImageData.fit_image_to_shape method. Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame."
type: docs
weight: 190
url: /python-net/aspose.words.drawing/imagedata/fit_image_to_shape/
---

## fit_image_to_shape() {#default}

Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame.


```python
def fit_image_to_shape(self):
    ...
```

### Examples

Shows hot to fit the image data to Shape frame.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert an image shape and leave its orientation in its default state.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=300, height=450)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Barcode.png')
shape.image_data.fit_image_to_shape()
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FitImageToShape.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

