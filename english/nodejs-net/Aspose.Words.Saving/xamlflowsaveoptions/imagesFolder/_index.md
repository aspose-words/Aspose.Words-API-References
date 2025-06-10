---
title: XamlFlowSaveOptions.imagesFolder property
linktitle: imagesFolder property
articleTitle: imagesFolder property
second_title: Aspose.Words for Node.js
description: "XamlFlowSaveOptions.imagesFolder property. Specifies the physical folder where images are saved when exporting a document to XAML format"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/xamlflowsaveoptions/imagesFolder/
---

## XamlFlowSaveOptions.imagesFolder property

Specifies the physical folder where images are saved when exporting a document to XAML format.
Default is an empty string.


```js
get imagesFolder(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.imagesFolder](./) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.imagesFolderAlias](../imagesFolderAlias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [XamlFlowSaveOptions.imagesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [XamlFlowSaveOptions.imagesFolder](./) property or provide custom streams via 
the [XamlFlowSaveOptions.imageSavingCallback](../imageSavingCallback/) event handler.




### See Also

* module [Aspose.Words.Saving](../../)
* class [XamlFlowSaveOptions](../)
* property [XamlFlowSaveOptions.imagesFolderAlias](../imagesFolderAlias/)
* property [XamlFlowSaveOptions.imageSavingCallback](../imageSavingCallback/)

