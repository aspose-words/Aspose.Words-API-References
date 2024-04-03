---
title: ImageType enumeration
linktitle: ImageType enumeration
articleTitle: ImageType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ImageType enumeration. Specifies the type (format) of an image in a Microsoft Word document."
type: docs
weight: 200
url: /python-net/aspose.words.drawing/imagetype/
---

## ImageType enumeration

Specifies the type (format) of an image in a Microsoft Word document.


### Members

| Name | Description |
| --- | --- |
| NO_IMAGE | The is no image data. |
| UNKNOWN | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| EMF | Windows Enhanced Metafile. |
| WMF | Windows Metafile. |
| PICT | Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported. |
| JPEG | JPEG JFIF. |
| PNG | Portable Network Graphics. |
| BMP | Windows Bitmap. |
| EPS | Encapsulated PostScript. |
| WEB_P | WebP. |

### Examples

Shows how to add an image to a shape and check its type.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

with open(IMAGE_DIR + "Logo.jpg", "rb") as stream:

    image = drawing.Image.from_stream(stream)

    # The image in the URL is a .gif. Inserting it into a document converts it into a .png.
    img_shape = builder.insert_image(image)
    self.assertEqual(aw.drawing.ImageType.JPEG, img_shape.image_data.image_type)
```

Shows how to read WebP image

```python
doc = Document(MY_DIR + "Document with WebP image.docx")
shape = doc.get_child(NodeType.SHAPE, 0, True).as_shape()

self.assertEqual(ImageType.WEB_P, shape.image_data.image_type)
```

### See Also

* module [aspose.words.drawing](../)
* property [ImageData.image_type](../imagedata/image_type/)

