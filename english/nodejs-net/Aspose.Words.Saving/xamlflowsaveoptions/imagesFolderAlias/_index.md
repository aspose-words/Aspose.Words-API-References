---
title: XamlFlowSaveOptions.imagesFolderAlias property
linktitle: imagesFolderAlias property
articleTitle: imagesFolderAlias property
second_title: Aspose.Words for Node.js
description: "XamlFlowSaveOptions.imagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into an XAML document"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/xamlflowsaveoptions/imagesFolderAlias/
---

## XamlFlowSaveOptions.imagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an XAML document.
Default is an empty string.


```js
get imagesFolderAlias(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.imagesFolder](../imagesFolder/) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.imagesFolderAlias](./) 
allows to specify how the image URIs will be constructed.

If [XamlFlowSaveOptions.imagesFolderAlias](./) is not an empty string, then the image URI written
to XAML will be *ImagesFolderAlias + \<image file name\>*.

If [XamlFlowSaveOptions.imagesFolderAlias](./) is an empty string, then the image URI written 
to XAML will be *ImagesFolder + \<image file name\>*.

If [XamlFlowSaveOptions.imagesFolderAlias](./) is set to '.' (dot), then the image file name 
will be written to XAML without path regardless of other options.




### See Also

* module [Aspose.Words.Saving](../../)
* class [XamlFlowSaveOptions](../)
* property [XamlFlowSaveOptions.imagesFolder](../imagesFolder/)
* property [XamlFlowSaveOptions.imageSavingCallback](../imageSavingCallback/)

