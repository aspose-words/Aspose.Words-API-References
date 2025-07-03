---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize method
linktitle: get_ScaleImageToShapeSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize method. Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is true in C++.'
type: docs
weight: 46000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Remarks


An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The [ScaleImageToShapeSize](./) property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [ScaleImageToShapeSize](./) is **true**, the image is scaled by [Aspose.Words](../../../aspose.words/) using high quality scaling during export to HTML. When [ScaleImageToShapeSize](./) is **false**, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when [ScaleImageToShapeSize](./) is **true**, but better printing quality and faster conversion when [ScaleImageToShapeSize](./) is **false**.

In addition to shapes containing individual raster images, this option also affects group shapes consisting of raster images. If [ScaleImageToShapeSize](./) is **false** and a group shape contains raster images whose intrinsic resolution is higher than the value specified in [ImageResolution](../get_imageresolution/), Aspose.Words will increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution images when saving to HTML.

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
