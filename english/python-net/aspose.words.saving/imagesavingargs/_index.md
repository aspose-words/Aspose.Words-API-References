---
title: ImageSavingArgs class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides data for the [IImageSavingCallback.image_saving()](../iimagesavingcallback/image_saving/#imagesavingargs) event"
type: docs
weight: 390
url: /python-net/aspose.words.saving/imagesavingargs/
---

## ImageSavingArgs class

Provides data for the [IImageSavingCallback.image_saving()](../iimagesavingcallback/image_saving/#imagesavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.




By default, when Aspose.Words saves a document to HTML, it saves each image into 
a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name
for each image found in the document.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to 
completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the 
[ImageSavingArgs.image_file_name](./image_file_name/), [ImageSavingArgs.current_shape](./current_shape/) and [ImageSavingArgs.is_image_available](./is_image_available/) 
properties.

To save images into streams instead of files, use the [ImageSavingArgs.image_stream](./image_stream/) property.




### Properties

| Name | Description |
| --- | --- |
| [current_shape](./current_shape/) | Gets the [ShapeBase](../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape  that is about to be saved. |
| [document](./document/) | Gets the document object that is currently being saved. |
| [image_file_name](./image_file_name/) | Gets or sets the file name (without path) where the image will be saved to. |
| [image_stream](./image_stream/) | Allows to specify the stream where the image will be saved to. |
| [is_image_available](./is_image_available/) | Returns ``True`` if the current image is available for export. |
| [keep_image_stream_open](./keep_image_stream_open/) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |

### See Also

* module [aspose.words.saving](../)

