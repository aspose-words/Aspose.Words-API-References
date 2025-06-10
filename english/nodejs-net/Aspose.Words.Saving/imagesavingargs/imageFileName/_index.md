---
title: ImageSavingArgs.imageFileName property
linktitle: imageFileName property
articleTitle: imageFileName property
second_title: Aspose.Words for Node.js
description: "ImageSavingArgs.imageFileName property. Gets or sets the file name (without path) where the image will be saved to."
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/imagesavingargs/imageFileName/
---

## ImageSavingArgs.imageFileName property

Gets or sets the file name (without path) where the image will be saved to.


```js
get imageFileName(): string
```

### Remarks

This property allows you to redefine how the image file names are generated
during export to HTML.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the image into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded image when 
exporting to HTML format. How the image file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated image file name looks like 
*\<document base file name\>.\<image number\>.\<extension\>*.

When saving a document to a stream, the generated image file name looks like 
*Aspose.Words.\<document guid\>.\<image number\>.\<extension\>*.

[ImageSavingArgs.imageFileName](./) must contain only the file name without the path.
Aspose.Words determines the path for saving and the value of the ``src`` attribute for writing 
to HTML using the document file name, the [HtmlSaveOptions.imagesFolder](../../htmlsaveoptions/imagesFolder/) and
[HtmlSaveOptions.imagesFolderAlias](../../htmlsaveoptions/imagesFolderAlias/) properties.




### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSavingArgs](../)
* property [ImageSavingArgs.currentShape](../currentShape/)
* property [ImageSavingArgs.isImageAvailable](../isImageAvailable/)
* property [HtmlSaveOptions.imagesFolder](../../htmlsaveoptions/imagesFolder/)
* property [HtmlSaveOptions.imagesFolderAlias](../../htmlsaveoptions/imagesFolderAlias/)

