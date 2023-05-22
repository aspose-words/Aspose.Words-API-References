---
title: RtfSaveOptions.save_images_as_wmf property
linktitle: save_images_as_wmf property
articleTitle: save_images_as_wmf property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_images_as_wmf property. When ``True`` all images will be saved as WMF."
type: docs
weight: 50
url: /python-net/aspose.words.saving/rtfsaveoptions/save_images_as_wmf/
---

## RtfSaveOptions.save_images_as_wmf property

When ``True`` all images will be saved as WMF.


This option might help to avoid WordPad warning messages.


### Examples

Shows how to convert all images in a document to the Windows Metafile format as we save the document as an RTF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Jpeg image:")
image_shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")

self.assertEqual(aw.drawing.ImageType.JPEG, image_shape.image_data.image_type)

builder.insert_paragraph()
builder.writeln("Png image:")
image_shape = builder.insert_image(IMAGE_DIR + "Transparent background logo.png")

self.assertEqual(aw.drawing.ImageType.PNG, image_shape.image_data.image_type)

# Create an "RtfSaveOptions" object to pass to the document's "save" method to modify how we save it to an RTF.
rtf_save_options = aw.saving.RtfSaveOptions()

# Set the "save_images_as_wmf" property to "True" to convert all images in the document to WMF as we save it to RTF.
# Doing so will help readers such as WordPad to read our document.
# Set the "save_images_as_wmf" property to "False" to preserve the original format of all images in the document
# as we save it to RTF. This will preserve the quality of the images at the cost of compatibility with older RTF readers.
rtf_save_options.save_images_as_wmf = save_images_as_wmf

doc.save(ARTIFACTS_DIR + "RtfSaveOptions.save_images_as_wmf.rtf", rtf_save_options)

doc = aw.Document(ARTIFACTS_DIR + "RtfSaveOptions.save_images_as_wmf.rtf")

shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)

if save_images_as_wmf:
    self.assertEqual(aw.drawing.ImageType.WMF, shapes[0].as_shape().image_data.image_type)
    self.assertEqual(aw.drawing.ImageType.WMF, shapes[1].as_shape().image_data.image_type)
else:

    self.assertEqual(aw.drawing.ImageType.JPEG, shapes[0].as_shape().image_data.image_type)
    self.assertEqual(aw.drawing.ImageType.PNG, shapes[1].as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

