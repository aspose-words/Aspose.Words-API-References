---
title: HtmlSaveOptions.scale_image_to_shape_size property
linktitle: scale_image_to_shape_size property
articleTitle: scale_image_to_shape_size property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.scale_image_to_shape_size property. Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB"
type: docs
weight: 460
url: /python-net/aspose.words.saving/htmlsaveoptions/scale_image_to_shape_size/
---

## HtmlSaveOptions.scale_image_to_shape_size property

Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML
or EPUB.
Default value is ``True``.


An image in a Microsoft Word document is a shape. The shape has a size and the image
has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, 
but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size.
The [HtmlSaveOptions.scale_image_to_shape_size](./) property controls where the scaling of the image
takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [HtmlSaveOptions.scale_image_to_shape_size](./) is ``True``, the image is scaled by Aspose.Words
using high quality scaling during export to HTML. When [HtmlSaveOptions.scale_image_to_shape_size](./) 
is ``False``, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better 
display quality in the browser and smaller file size when [HtmlSaveOptions.scale_image_to_shape_size](./) is ``True``, 
but better printing quality and faster conversion when [HtmlSaveOptions.scale_image_to_shape_size](./) is ``False``.

In addition to shapes containing individual raster images, this option also affects group shapes consisting
of raster images. If [HtmlSaveOptions.scale_image_to_shape_size](./) is ``False`` and a group shape contains raster images
whose intrinsic resolution is higher than the value specified in [HtmlSaveOptions.image_resolution](../image_resolution/), Aspose.Words will
increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution
images when saving to HTML.




### Examples

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a shape which contains an image, and then make that shape considerably smaller than the image.
image = drawing.Image.from_file(IMAGE_DIR + "Transparent background logo.png")

self.assertEqual(400, image.size.width)
self.assertEqual(400, image.size.height)

image_shape = builder.insert_image(image)
image_shape.width = 50
image_shape.height = 50

# Saving a document that contains shapes with images to HTML will create an image file in the local file system
# for each such shape. The output HTML document will use <image> tags to link to and display these images.
# When we save the document to HTML, we can pass a SaveOptions object to determine
# whether to scale all images that are inside shapes to the sizes of their shapes.
# Setting the "scale_image_to_shape_size" flag to "True" will shrink every image
# to the size of the shape that contains it, so that no saved images will be larger than the document requires them to be.
# Setting the "scale_image_to_shape_size" flag to "False" will preserve these images' original sizes,
# which will take up more space in exchange for preserving image quality.
options = aw.saving.HtmlSaveOptions()
options.scale_image_to_shape_size = scale_image_to_shape_size

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.scale_image_to_shape_size.html", options)

file_size = os.path.getsize(ARTIFACTS_DIR + "HtmlSaveOptions.scale_image_to_shape_size.001.png")

if scale_image_to_shape_size:
    self.assertGreater(10000, file_size)
else:
    self.assertLess(30000, file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.image_resolution](../image_resolution/)

