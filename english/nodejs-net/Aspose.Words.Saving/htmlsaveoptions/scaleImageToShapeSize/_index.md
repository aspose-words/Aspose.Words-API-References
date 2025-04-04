---
title: HtmlSaveOptions.scaleImageToShapeSize property
linktitle: scaleImageToShapeSize property
articleTitle: scaleImageToShapeSize property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.scaleImageToShapeSize property. Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB"
type: docs
weight: 460
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/scaleImageToShapeSize/
---

## HtmlSaveOptions.scaleImageToShapeSize property

Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML
or EPUB.
Default value is ``true``.



```js
get scaleImageToShapeSize(): boolean
```

### Remarks

An image in a Microsoft Word document is a shape. The shape has a size and the image
has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, 
but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size.
The [HtmlSaveOptions.scaleImageToShapeSize](./) property controls where the scaling of the image
takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [HtmlSaveOptions.scaleImageToShapeSize](./) is ``true``, the image is scaled by Aspose.Words
using high quality scaling during export to HTML. When [HtmlSaveOptions.scaleImageToShapeSize](./) 
is ``false``, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better 
display quality in the browser and smaller file size when [HtmlSaveOptions.scaleImageToShapeSize](./) is ``true``, 
but better printing quality and faster conversion when [HtmlSaveOptions.scaleImageToShapeSize](./) is ``false``.

In addition to shapes containing individual raster images, this option also affects group shapes consisting
of raster images. If [HtmlSaveOptions.scaleImageToShapeSize](./) is ``false`` and a group shape contains raster images
whose intrinsic resolution is higher than the value specified in [HtmlSaveOptions.imageResolution](../imageResolution/), Aspose.Words will
increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution
images when saving to HTML.




### Examples

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a shape which contains an image, and then make that shape considerably smaller than the image.
let imageShape = builder.insertImage(base.imageDir + "Transparent background logo.png");
imageShape.width = 50;
imageShape.height = 50;

// Saving a document that contains shapes with images to HTML will create an image file in the local file system
// for each such shape. The output HTML document will use <image> tags to link to and display these images.
// When we save the document to HTML, we can pass a SaveOptions object to determine
// whether to scale all images that are inside shapes to the sizes of their shapes.
// Setting the "ScaleImageToShapeSize" flag to "true" will shrink every image
// to the size of the shape that contains it, so that no saved images will be larger than the document requires them to be.
// Setting the "ScaleImageToShapeSize" flag to "false" will preserve these images' original sizes,
// which will take up more space in exchange for preserving image quality.
let options = new aw.Saving.HtmlSaveOptions();
options.scaleImageToShapeSize = scaleImageToShapeSize;

doc.save(base.artifactsDir + "HtmlSaveOptions.scaleImageToShapeSize.html", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.imageResolution](../imageResolution/)

