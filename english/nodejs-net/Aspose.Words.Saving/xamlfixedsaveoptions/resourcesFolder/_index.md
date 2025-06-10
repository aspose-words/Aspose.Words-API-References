---
title: XamlFixedSaveOptions.resourcesFolder property
linktitle: resourcesFolder property
articleTitle: resourcesFolder property
second_title: Aspose.Words for Node.js
description: "XamlFixedSaveOptions.resourcesFolder property. Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/xamlfixedsaveoptions/resourcesFolder/
---

## XamlFixedSaveOptions.resourcesFolder property

Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format.
Default is ``null``.



```js
get resourcesFolder(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all
images embedded in the document as standalone files. [XamlFixedSaveOptions.resourcesFolder](./)
allows you to specify where the images will be saved and [XamlFixedSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the
images in the same folder where the document file is saved. Use [XamlFixedSaveOptions.resourcesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images,
but still needs to save the images somewhere. In this case, you need to specify an accessible folder
by using the [XamlFixedSaveOptions.resourcesFolder](./) property




### See Also

* module [Aspose.Words.Saving](../../)
* class [XamlFixedSaveOptions](../)
* property [XamlFixedSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)

