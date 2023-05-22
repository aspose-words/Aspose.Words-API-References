---
title: LoadOptions.base_uri property
linktitle: base_uri property
articleTitle: base_uri property
second_title: Aspose.Words for Python
description: "LoadOptions.base_uri property. Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required"
type: docs
weight: 20
url: /python-net/aspose.words.loading/loadoptions/base_uri/
---

## LoadOptions.base_uri property

Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required.
Can be ``None`` or empty string. Default is ``None``.


This property is used to resolve relative URIs into absolute in the following cases:


1. When loading an HTML document from a stream and the document contains images with
   relative URIs and does not have a base URI specified in the BASE HTML element.
   
1. When saving a document to PDF and other formats, to retrieve images linked using relative URIs
   so the images can be saved into the output document.
   



### Examples

Shows how to open an HTML document with images from a stream using a base URI.

```python
with open(MY_DIR + "Document.html", "rb") as stream:
    # Pass the URI of the base folder while loading it
    # so that any images with relative URIs in the HTML document can be found.
    load_options = aw.loading.LoadOptions()
    load_options.base_uri = IMAGE_DIR

    doc = aw.Document(stream, load_options)

    # Verify that the first shape of the document contains a valid image.
    shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

    self.assertTrue(shape.is_image)
    self.assertIsNotNone(shape.image_data.image_bytes)
    self.assertAlmostEqual(32.0, aw.ConvertUtil.point_to_pixel(shape.width), delta=0.01)
    self.assertAlmostEqual(32.0, aw.ConvertUtil.point_to_pixel(shape.height), delta=0.01)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

