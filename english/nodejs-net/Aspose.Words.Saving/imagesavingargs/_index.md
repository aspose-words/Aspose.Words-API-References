---
title: ImageSavingArgs class
linktitle: ImageSavingArgs class
articleTitle: ImageSavingArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.ImageSavingArgs class. Provides data for the [IImageSavingCallback.imageSaving()](../iimagesavingcallback/imageSaving/#imagesavingargs) event"
type: docs
weight: 380
url: /nodejs-net/aspose.words.saving/imagesavingargs/
---

## ImageSavingArgs class

Provides data for the [IImageSavingCallback.imageSaving()](../iimagesavingcallback/imageSaving/#imagesavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

By default, when Aspose.Words saves a document to HTML, it saves each image into 
a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name
for each image found in the document.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to 
completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the 
[ImageSavingArgs.imageFileName](./imageFileName/), [ImageSavingArgs.currentShape](./currentShape/) and [ImageSavingArgs.isImageAvailable](./isImageAvailable/) 
properties.

To save images into streams instead of files, use the Aspose.Words.Saving.ImageSavingArgs.ImageStream property.




### Properties

| Name | Description |
| --- | --- |
| [currentShape](./currentShape/) | Gets the [ShapeBase](../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape  that is about to be saved. |
| [document](./document/) | Gets the document object that is currently being saved. |
| [imageFileName](./imageFileName/) | Gets or sets the file name (without path) where the image will be saved to. |
| [isImageAvailable](./isImageAvailable/) | Returns ``true`` if the current image is available for export. |
| [keepImageStreamOpen](./keepImageStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |

### See Also

* module [Aspose.Words.Saving](../)

