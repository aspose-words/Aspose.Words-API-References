---
title: convert_metafiles_to_png property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets whether to convert metafile (Aspose.FileFormat.Wmf or Aspose.FileFormat.Emf) images to Aspose.FileFormat.Png image format."
type: docs
weight: 30
url: /python-net/aspose.words.loading/loadoptions/convert_metafiles_to_png/
---

## LoadOptions.convert_metafiles_to_png property

Gets or sets whether to convert metafile (Aspose.FileFormat.Wmf or Aspose.FileFormat.Emf) images to Aspose.FileFormat.Png image format.


Metafiles (Aspose.FileFormat.Wmf or Aspose.FileFormat.Emf) is an uncompressed image format and sometimes requires to much RAM to hold and process document.
This option allows to convert all metafile images to Aspose.FileFormat.Png on document loading.
Please note - conversion vector graphics to raster decreases quality of the images.



### Examples

Shows how to convert WMF/EMF to PNG during loading document.

```python
doc = aw.Document()

shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
shape.image_data.set_image(IMAGE_DIR + "Windows MetaFile.wmf")
shape.width = 100
shape.height = 100

doc.first_section.body.first_paragraph.append_child(shape)

doc.save(ARTIFACTS_DIR + "Image.convert_metafiles_to_png.docx")

shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

self.verify_image_in_shape(1600, 1600, aw.drawing.ImageType.WMF, shape)

load_options = aw.loading.LoadOptions()
load_options.convert_metafiles_to_png = True

doc = aw.Document(ARTIFACTS_DIR + "Image.convert_metafiles_to_png.docx", load_options)
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

self.verify_image_in_shape(1666, 1666, aw.drawing.ImageType.PNG, shape)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

